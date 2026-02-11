# simple agent demo
  only for three modes : summary , code and chat

# If you only want to use the js version,
  ## Usage: node agent.js project_dir "task"  (the task must use " ")
    # before you run the agent.js
    you MUST export:
    export LLM_BASE_URL='https://your_LLM_base_URL'
    export LLM_API_KEY='your_API_key'
    export LLM_MODEL='your_LLM_name'
    # then run the demo:
    for example: node agent.js ./text "帮我总结一下这个目录里面所有.js文件都讲了什么"
    
  like a test in my local:
    node agent.js ./text "帮我总结一下这个目录里面所有.js文件都讲了什么"
    RAG hits: a.js#0(0), a.js#1(0), a.js#2(0), a.js#3(0), a.js#4(0), a.js#5(0), a.js#6(0), a.js#7(0)
    {
      "summary": "这是一个基于RAG（检索增强生成）的代码分析工具，实现了智能代码理解和辅助功能。系统通过递归扫描项目文件，使用相关性评分算法选择最相关的文件，然后构建针对不同任务的提示词，最终调用大语言模型进行代码分析或修改建议。支持两种工作模式：项目总结模式和代码修改模式。",
      "key_files": [
        "a.js"
      ],
      "entrypoints": [
        "a.js"
      ]
    }

## if using Chinese, Chinese language task must lead low hit rate like that example (now (2/11/2026) in the demo, LLM will rewrite the task , so this is wrong)
    a.js#0(0), a.js#1(0), a.js#2(0), a.js#3(0), a.js#4(0), a.js#5(0), a.js#6(0), a.js#7(0)

## 2/11/2026: rewrite by TS(You only need to download .ts and .json files.)
  # if you want run by TS ,the types.js is ready, and you MUST need the shell:
  cd /yourDir
  npm install
  npm run build
  then(run the demo):
  npm install
  npm run build
  # before you run the agent.js
  you MUST export:
  export LLM_BASE_URL='https://your_LLM_base_URL'
  export LLM_API_KEY='your_API_key'
  export LLM_MODEL='your_LLM_name'
  # in the last:
  node dist/agent.js /yourDir "summary the files in this dir"
  the explanation:
  node dist/agent.js  /yourDir(must be a dir) " your task"(must use " ")
  
