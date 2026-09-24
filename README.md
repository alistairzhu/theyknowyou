# They Know You

A single prompt that compiles a **portable memory snapshot** of you — so you stop losing context every time you switch AI assistants.

---

## English

### The problem

Every AI assistant builds up an implicit picture of you: your stack, your tone preferences, the people you mention, the projects you keep circling back to. That picture lives inside one vendor's chat history. Start a new assistant and you are a stranger again — and re-explaining yourself for two weeks is exactly the tax nobody budgets for.

### The fix

Hand [`PROMPT.md`](./PROMPT.md) to the assistant you have already been using for a while. It will read back through your past conversations and distill what it reliably knows about you into one Markdown block, organised into fixed sections: identity, work, communication preferences, recurring people, ongoing projects, tools, and so on.

Paste that block into your new assistant's memory or custom-instructions field. It starts oriented instead of blank.

### How to use it

1. Open the assistant that already knows you.
2. Copy the entire contents of [`PROMPT.md`](./PROMPT.md) and send it as a message.
3. Collect the Markdown output.
4. **Read it. Fix what is wrong, cut what you would rather not carry forward.** The prompt tells the model to skip sensitive topics unless you asked it to remember them, but it is your data — verify it yourself.
5. Paste the cleaned version into the new assistant's memory slot.

### What makes the output usable

- **Structured, not chatty.** Fixed section headers, one fact per bullet, no filler narrative — it survives being re-read by a different model.
- **Honest about uncertainty.** Anything the model is guessing is tagged `(inferred)`, so you know which lines to scrutinise.
- **Empty beats fake.** Sections with nothing solid get omitted rather than padded with invented placeholders.
- **Bounded.** Hard cap of 2000 words, because a memory that does not fit in a context window is not a memory.
- **Sensitive by default.** Health, finances, and mental health stay out unless you explicitly asked otherwise.

### Works with

Any assistant that has meaningful conversation history and can write Markdown. No API keys, no scripts, no vendor lock-in — it is just a prompt.

### A note on privacy

The output is a profile of you. Keep it out of public repos, and think twice before pasting it into a service you would not otherwise tell these things to. This repository contains the *prompt*, not anyone's memory.

### License

Public domain / CC0 — copy it, fork it, change the sections to fit your life.

---

## 中文

### 问题

每个 AI 助手都会在长期对话里悄悄攒出一份关于你的画像：你的技术栈、你喜欢的语气、你常提到的人、你反复推进的项目。这份画像被锁在某一家的聊天记录里。一旦换助手，你又变回陌生人——而重新解释自己这件事，两周的时间成本没人提前预算过。

### 解法

把 [`PROMPT.md`](./PROMPT.md) 发给你已经用了很久的那个助手。它会回读你们的历史对话，把「它确实知道的关于你的事」压缩成一段 Markdown，按固定板块组织：身份、工作、沟通偏好、常提及的人、进行中的项目、常用工具等。

把这段 Markdown 粘进新助手的记忆区或自定义指令里。它一开始就是「有背景的」，而不是空白。

### 使用步骤

1. 打开那个已经比较了解你的助手。
2. 复制 [`PROMPT.md`](./PROMPT.md) 的全部内容，作为一条消息发出去。
3. 收下它输出的 Markdown。
4. **读一遍。改掉不对的，删掉你不想带走的。** 提示词里已经要求模型跳过敏感话题（除非你明确要求记住），但这是你的数据，请自己把关。
5. 把清理后的版本粘进新助手的记忆槽位。

### 为什么这个输出好用

- **结构化，不闲聊。** 固定小标题、一条一个事实、不写过渡句——换一个模型读也读得懂。
- **对不确定性诚实。** 模型靠猜的内容一律标注 `(inferred)`，你就知道哪几行需要重点核对。
- **宁可留白，不要编造。** 没有实锤的板块直接省略，而不是拿假占位符凑数。
- **有上限。** 硬性 2000 词封顶——塞不进上下文窗口的记忆不叫记忆。
- **默认规避敏感信息。** 健康、财务、心理状态默认不写入，除非你明确要求。

### 适用于

任何有实质对话历史、且能输出 Markdown 的助手。不需要 API key，不需要脚本，不绑定任何厂商——它只是一段提示词。

### 关于隐私

输出结果是你的个人画像。别放进公开仓库，也别随手上传给一个你本来不会告诉它这些事的服务。本仓库里放的是**提示词本身**，不是任何人的记忆。

### 许可

公有领域 / CC0——随便复制、fork，按你自己的情况改板块。
