# React Chrome Extension Template
ReactでChrome拡張を開発するためのテンプレート

### Package
- "react": "^17.0.2",
- "typescript": "^4.1.2"
- "node-sass": "^5.0.0",

## 使い方
1. Chrome拡張のボタンから"拡張機能を管理"を開く
2. "パッケージ化されていない拡張機能を読み込む"をクリックしてbuildディレクトリを選択
3. 新しいタブを開くと以下のようなエラーが出てきます

```

Refused to execute inline script because it violates the following Content Security Policy directive: "script-src 'self' 'sha256-xxx'". Either the 'unsafe-inline' keyword, a hash ('sha256-*****'), or a nonce ('nonce-...') is required to enable inline execution.

```

```public/manifesct.json```の```content_security_policy```の```'sha256-xxx'```の部分をエラー文の```sha256-*****```に置き換える

4. もう一度buildしてページを読み込むとファイルが見れます