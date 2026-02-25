# remotion-editor
- ファイル構成（Desktop/claude code）
```
remotion-editor/
├── src/
│   ├── index.ts
│   ├── Root.tsx
│   └── compositions/
│       ├── HelloWorld.tsx    # タイトルアニメーション
│       ├── Slideshow.tsx     # 画像スライドショー
│       └── TextAnimation.tsx # テキストアニメーション
├── out/                      # MP4 出力先
├── Dockerfile
├── docker-compose.yml
└── README.md
```
## 使用方法
- Studio 起動（ブラウザで編集・プレビュー）
```
cd ~/Desktop/claudecode/remotion-editor
docker compose up studio
→ ブラウザで http://localhost:3000 を開く
```

- MP4 レンダリング
```
# HelloWorld をレンダリング
docker compose run --rm render HelloWorld out/HelloWorld.mp4

# スライドショー
docker compose run --rm render Slideshow out/Slideshow.mp4

# テキストアニメーション
docker compose run --rm render TextAnimation out/TextAnimation.mp4
```
