# SBTI Test — CTO Agent 指令

## 项目概述
SBTI 人格测试，三语版本（中/英/日），部署在 sbti.evermemory.ai。
纯静态 HTML，无构建步骤，通过 Vercel 部署。

## 目录结构
```
sbti-test/
├── index.html      ← 中文版（原版）
├── en/index.html   ← English 版
├── ja/index.html   ← 日本語版
├── image/          ← 27种人格类型配图（PNG/JPG）
└── CLAUDE.md
```

## 部署
- 平台：Vercel，连接 GitHub repo
- 域名：sbti.evermemory.ai → CNAME cname.vercel-dns.com
- 无构建步骤，Framework Preset: Other

## 三语内容规范

### 人格类型 code 映射
| Code | 中文名 | English | 日本語 |
|------|--------|---------|--------|
| CTRL | 拿捏者 | The Controller | 支配者 |
| BOSS | 领导者 | The Leader | リーダー |
| SEXY | 尤物 | The Charmer | 魅惑の人 |
| FAKE | 伪人 | The Shapeshifter | 偽者 |
| WOC! | 握草人 | OMG Person | えっマジ人 |
| MALO | 吗喽 | The Minion | 手下 |
| Dior-s | 屌丝 | The Wise Slacker | 賢者的底辺 |
| DRUNK | 酒鬼 | The Drunk | 飲んだくれ |
| HHHH | 傻乐者 | The Chaotic | カオス |
| (其余见各 index.html) | - | - | - |

### 修改内容时注意
- 三个 HTML 是独立文件，修改一处需同步更新另外两处
- 图片路径：index.html 用 `./image/`，en/ 和 ja/ 用 `../image/`
- 中文特有文化梗（白酒、B站、屌丝）在英/日版已做本地化处理，修改时保持各语言的本地化风格

## 分支规则
- 改动只推 `dev`，禁止直接推 `main`
- merge 到 main 需 CEO 决策
