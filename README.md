# Project Sekai Scores

プロセカの譜面ファイル解析し、ベクトル画像（SVG）を生成する。

## Installation

pip でインストール：

```
pip install pjsekai.scores
```

また、手動でビルドしてインストール：

```
python -m build
pip install dist/pjsekai.scores-*.whl
```

## Usage

Project Sekai Scores には、デフォルトの起動スクリプトが含まれており、ローカルの SUS 譜面ファイルを読み込み、それを SVG ベクター画像に変換することができます。以下のコマンドを使って簡単に実行できます：

```
python -m pjsekai.scores <xxx.sus>
```

以下はパッケージとして使用して譜面画像を生成する例です：

```python
import pjsekai.scores

score = pjsekai.scores.Score.open('1.sus', encoding='UTF-8')
drawing = pjsekai.scores.Drawing(score=score)
drawing.svg().saveas('1.svg')
```

譜面ファイルを個性化して豊かにするカスタマイズ機能を提供しています。下記の文書をご参照ください：

* [BPM、拍子、セクションを変換]()

* [歌詞を追加]()

* [スタイルシートをカスタマイズ]()

## License

Project Sekai Scores は MIT ライセンスのもとで提供されています。詳細については、[LICENSE](LICENSE) ファイルをご覧ください。

Project Sekai Scores は SEGA・Colorful Palette・プロジェクトセカイとは一切関係がありません。
