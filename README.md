# Project Sekai Scores

プロセカの譜面ファイル解析し、ベクトル画像（SVG）を生成する。

## Installation

pip でインストール：

```
pip install sekaiworld.scores
```

また、手動でビルドしてインストール：

```
uv sync --all-groups
uv run python -m build
uv pip install dist/sekaiworld.scores-*.whl
```

## Usage

Project Sekai Scores には、デフォルトの起動スクリプトが含まれており、ローカルの SUS 譜面ファイルを読み込み、それを SVG ベクター画像に変換することができます。以下のコマンドを使って簡単に実行できます：

```
uv run python -m sekaiworld.scores <xxx.sus>
```

以下はパッケージとして使用して譜面画像を生成する例です：

```python
import sekaiworld.scores

score = sekaiworld.scores.Score.open('1.sus', encoding='UTF-8')
drawing = sekaiworld.scores.Drawing(score=score)
drawing.svg().saveas('1.svg')
```

譜面ファイルを個性化して豊かにするカスタマイズ機能を提供しています。下記の文書をご参照ください：

* [BPM、拍子、セクションを変換](https://gitlab.com/pjsekai/scores/-/wikis/rebase)

* [歌詞を追加](https://gitlab.com/pjsekai/scores/-/wikis/lyric)

* [スタイルシートをカスタマイズ](https://gitlab.com/pjsekai/scores/-/wikis/css)

## License

Project Sekai Scores は MIT ライセンスのもとで提供されています。詳細については、[LICENSE](LICENSE) ファイルをご覧ください。

Project Sekai Scores は SEGA・Colorful Palette・プロジェクトセカイとは一切関係がありません。
