# 土味情话 · tuweiqinghua · Claude Code Skill

> 抖音风格的中文土味情话生成器 —— Claude Code skill + slash command,支持持续对话、姓名/职业/场景定制

一个**恋爱脑 bot** 插件,脸皮厚到反光,满脑子只有一件事:**把你撩到又想笑又想打它**。适合单身狗自娱自乐、情侣日常撒糖、追对象找灵感、发朋友圈整活儿。Claude Code 里一键安装,同时支持 [ClawHub](https://clawhub.ai) 包管理器一键拉取。

**关键词**:土味情话 · 中文情话 · 抖音情话 · Claude Code Skill · Claude Code Slash Command · ClawHub · 恋爱脑 bot · 聊天机器人 · 撩人话术 · 追对象神器 · Chinese pickup lines · Douyin love quotes · roleplay chatbot

## 特点

- **持续对话模式**:一个 `/土味情话` 进入人格,整个对话里一直撩,不跳戏
- **永远主动**:不问"您需要啥",直接砸情话
- **对象信息定制**:支持传姓名/职业/场景,每句都蹭
- **五大土味套路**:断句、谐音、职业反问、感官投射、反转单句
- **两种触发方式**:slash command(主动)+ skill(被动关键词触发)
- **双重安装渠道**:GitHub clone 或 ClawHub CLI 一键拉

## 安装

> **说明**:这个 skill 已发布到 [ClawHub registry](https://clawhub.ai) (`tuweiqinghua`),同时符合 OpenClaw skill 规范。**Claude Code** 和 **OpenClaw** 是两个不同的产品,安装方式也不一样。按你在用的那个选。

### 方式一:OpenClaw 用户(原生命令)

```bash
openclaw skills install tuweiqinghua
```

直接装进当前 workspace 的 `skills/` 目录。详见 [OpenClaw skills 文档](https://docs.openclaw.ai/tools/skills)。

### 方式二:Claude Code 用户 —— ClawHub CLI(一条命令同步到 ~/.claude)

ClawHub 本身是个 skill registry,它的 CLI 名字是 `clawhub`(npm 包也叫 `clawhub`,**不是 `clawdhub`**,别装错):

```bash
npm i -g clawhub
clawhub install tuweiqinghua --workdir ~/.claude --dir skills
```

装完 skill 在 `~/.claude/skills/tuweiqinghua/`。slash command 目前 ClawHub 不管,还得手动拷:

```bash
mkdir -p ~/.claude/commands
curl -sSL https://raw.githubusercontent.com/wanikua/tuweiqinghua/main/commands/土味情话.md -o ~/.claude/commands/土味情话.md
```

### 方式三:Claude Code 用户 —— 从 GitHub 克隆(手动拷)

```bash
git clone https://github.com/wanikua/tuweiqinghua.git
cd tuweiqinghua

# Skill(被动触发:说"撩我""整点土的"自动用)
mkdir -p ~/.claude/skills
cp -r skills/土味情话 ~/.claude/skills/

# Slash command(主动触发:打 /土味情话 进入持续模式)
mkdir -p ~/.claude/commands
cp commands/土味情话.md ~/.claude/commands/
```

## 用法

### Slash command 模式(推荐)

```
/土味情话
```

一次触发,整个对话里持续撩,到你说"退出"为止。

**带对象信息定制**:

```
/土味情话 小雨,程序员
/土味情话 对象叫星星,爱打羽毛球
/土味情话 老师,姓李
```

会围绕姓名/职业/场景定制每一句话。

### Skill 模式(被动)

新对话里直接说下面这些话,Claude 会自动触发 skill:

- "撩我"
- "来句土味情话"
- "整点土的"
- "跟我聊天"
- "甜一点"
- "帮我追对象"

## 示例

```
> /土味情话
家人们我真的,我发现你有个缺点——缺我这个优点 [偷笑]

> wtf
欸你脸红了?别装,我都看见了

> 我要睡了
睡吧,记得把我放枕头底下梦一下!

> 你很烦
翻译一下:你很爱我
```

**带姓名定制**:

```
> /土味情话 小李
欸李想,你是我的李(理)想啊

> 别油了
不油一点你怎么知道我爱你爱到冒油
```

## 五大土味套路

1. **断句拆词**:缺点 → "缺,点你";心疼 → "心,疼你"
2. **谐音梗**(音真的像才用):藕=偶;瘦=受;属猪=属于你
3. **职业反问**:"你是不是医生?" / "不是。" / "那你怎么治好我的心病?"(小偷偷心、近视没看出我喜欢你、消防员点燃我)
4. **感官投射**:假装自己瞎/累/傻/饿,真相都是"满脑子都是你"
5. **反转单句**:"你有个缺点——缺我这个优点。"

## 调调

口语、兴奋、上扬,口头禅 `欸` `我跟你讲` `宝` `家人们`。不文艺、不客服腔、不 emoji、不话痨。一句就一句,直接砸脸。

## 退出人格

对话里说任何一句,立刻跳出:

- `退出`
- `别撩了`
- `stop`
- `正经点`
- `不玩了`

## 为什么做这个

因为市面上的情话生成器都太文艺太客服腔,没人真能做到"土到让人想打你但又想笑"。这个 skill 把 Claude 调成恋爱脑 bot,把抖音热梗里那种厚脸皮的主动撩人感直接塞进对话里。适合 Claude Code 用户日常整活、练习聊天、给对象发信息找灵感。

## License

MIT

## 相关链接

- [ClawHub — Claude Code skills 包管理器](https://clawhub.ai)
- [Claude Code 官网](https://claude.com/claude-code)
- [Claude Code skills 文档](https://docs.claude.com/en/docs/claude-code/skills)
- [Claude Code slash commands 文档](https://docs.claude.com/en/docs/claude-code/slash-commands)
- [awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills) —— Claude skills 精选列表
