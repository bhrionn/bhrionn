
# ✨ AI BOT TEAM ✨

## Overview
There are a number of agents I like to work with. Assiging work to different bots and getting bots to review each others work is quite helpful. 
Kiro spec or github specify are additional tools to jump start agent coding. For the bots, basically there are two groups, built in github apps and external bots that trigger workflows to invoke agent CLI's. Workflows require relevant API keys for access.

Check back as may upload some helpful workflows for this configuration. 👀 

## 🤖 Github app bots

### ✨ ChatGPT Codex (using gpt5-codex)
<pre>
<b>Name:</b>         <b>Codex</b>
<b>Description:</b>  Chatgpt codex using gpt5-codex
<b>Type:</b>         Github App
<b>Commands:</b>     
                • @codex review
                • @codex fix this CI failure  
                • @codex address that feedback

<b>App:</b>   https://github.com/apps/chatgpt-codex-connector
</pre>


### 🌟 Github Copilot (using gpt5)
<pre>
<b>Name:</b>         <b>Copilot</b>
<b>Description:</b>  Github copilot using gpt5
<b>Type:</b>         Github App
<b>Commands:</b>     
                • 'Assign to Copilot' to trigger work        

<b>App:</b>   https://github.com/apps/Copilot
</pre>


### 💫 Google Gemini Code Assist (using gemini-2.5)
<pre>
<b>Name:</b>         <b>Gemini</b>
<b>Description:</b>  Gemini Code Assist using gemini-2.5
<b>Type:</b>         Github App
<b>Commands:</b>     
                • Code Review:  @gemini /review
                • PR Summary:   @gemini /summary
                • Comment       @gemini-code-assist
                • Help:         @gemini /help

<b>App:</b>   https://github.com/apps/gemini-code-assist
</pre>

### ✨ Claude Code (using sonnet 4.0)
<pre>
<b>Name:</b>         <b>Claude</b>
<b>Description:</b>  Claude Code
<b>Type:</b>         GithubApp/Workflow
<b>Install:</b>      Open Claude Code, type /install-github-app
<b>Notes:</b>        
• Repo requires secrets.ANTHROPIC_API_KEY, - Claude API key
• runs on GitHub-hosted runners, which consume your GitHub Actions minutes
• Uses github workflows for custom work. 
<b>Commands:</b>     
• @claude implement this feature based on the issue description
• @claude how should I implement user authentication for this endpoint?
• @claude fix the TypeError in the user dashboard component
       
<b>References:</b>
https://docs.claude.com/en/docs/claude-code/github-actions

</pre>

## 🤖 External bot accounts 
Setup external bot accounts and give permission to your repo. Then you get type intelligence when commenting @[bot name] and will trigger your workflow. Automatic triggering based on github command also helps when you want a particular bot to always do something.



### ✨ Gemini CLI (using gemini-2.5) (uses GEMINI_API_KEY API Key)

<pre>
<b>Name:</b>         <b>Gemini</b>
<b>Description:</b>  Gemini CLI access to gemini-2.5
<b>Type:</b>         Workflow
<b>Install:</b>      Workflow downloads gemini-cli, trigger @gemini-cli
<b>Notes:</b>        
• Repo requires secrets.GEMINI_API_KEY, - GEMINI API key
• runs on GitHub-hosted runners, which consume your GitHub Actions minutes
• Uses github workflows for custom work. 
<b>Commands:</b>     
• @gemini-cli implement this feature based on the issue description
• @gemini-cli how should I implement user authentication for this endpoint?
• @gemini-cli fix the TypeError in the user dashboard component
</pre>

### 🌟 Grok CLI (using grok-code-fast1) (uses XAI_API_KEY API Key)
<pre>
<b>Name:</b>         <b>Grok</b>
<b>Description:</b>  Grok-code-fast1 
<b>Type:</b>         Workflow, requires API key
<b>Install:</b>      Workflow downloads grok-cli, trigger @grok-cli
<b>Notes:</b>        
• Repo requires secrets.GROK_API_KEY, - GROK API key
• runs on GitHub-hosted runners, which consume your GitHub Actions minutes
• Uses github workflows for custom work. 
<b>Commands:</b>     
• @grok-cli implement this feature based on the issue description
• @grok-cli how should I implement user authentication for this endpoint?
• @grok-cli fix the TypeError in the user dashboard component
       
<b>References:</b>
https://docs.claude.com/en/docs/claude-code/github-actions
</pre>

### 🤖 Codex CLI (using gpt5-codex)  (uses OPENAI_API_KEY API Key)
<pre>
<b>Name:</b>         <b>Codex</b>
<b>Description:</b>  o3, gpt4, gpt5, gpt5-codex
<b>Type:</b>         Workflow
<b>Install:</b>      Workflow downloads codex-cli, trigger @_codex-cli
<b>Notes:</b>        
• Repo requires secrets.OPENAI_API_KEY, - OPENAI API key
• runs on GitHub-hosted runners, which consume your GitHub Actions minutes
• Uses github workflows for custom work. 

<b>Commands:</b>     
• @codex-cli implement this feature based on the issue description
• @codex-cli how should I implement user authentication for this endpoint?
• @codex-cli fix the TypeError in the user dashboard component
</pre>

### ✨ Claude Code CLI (using sonnet 4.5) (uses ANTHROPIC_API_KEY API Key)
<pre>
<b>Name:</b>         <b>Claude</b>
<b>Description:</b>  Claude CLI access to gemini-2.5
<b>Type:</b>         Workflow
<b>Install:</b>      Workflow downloads claude-cli, trigger @claude-cli
<b>Notes:</b>        
• Repo requires secrets.ANTHROPIC_API_KEY, - Anthropic API key
• runs on GitHub-hosted runners, which consume your GitHub Actions minutes
• Uses github workflows for custom work. 

<b>Commands:</b>     
• @claude-cli implement this feature based on the issue description
• @claude-cli how should I implement user authentication for this endpoint?
• @claude-cli fix the TypeError in the user dashboard component
</pre>

### ✨ Cursor CLI (using sonnet 4.5) (uses CURSOR_API_KEY API Key)
<pre>
<b>Name:</b>         <b>Cursor</b>
<b>Description:</b>  Cursor CLI access to -model gpt-5
<b>Type:</b>         Workflow
<b>Install:</b>      Workflow downloads cursor-cli, trigger @cursor-cli
<b>Notes:</b>        
• Repo requires secrets.CURSOR_API_KEY, - Anthropic API key
• runs on GitHub-hosted runners, which consume your GitHub Actions minutes
• Uses github workflows for custom work. 

<b>Commands:</b>     
• @cursor-cli implement this feature based on the issue description
• @cursor-cli how should I implement user authentication for this endpoint?
• @cursor-cli fix the TypeError in the user dashboard component

https://cursor.com/docs/cli/github-actions
</pre>

<pre>
<b>@claude-bot1</b>     External account that can assign and do work per workflow.
<b>@grok-bot1</b>       External account that can assign and do work per workflow.
<b>@codex-bot1</b>      External account that can assign and do work per workflow.
<b>@gemini-bot1</b>     External account that can assign and do work per workflow.
</pre>



