# simple agent demo
  Using LLM: qwen3-coder-plus
  only for two modes : summary and code
  // summary need your task includes 总结 | summary | summarize
  ## Usage: node agent.js <project_dir> "<task>" 
  for example: node agent.js ./text "帮我总结一下这个目录里面所有.js文件都讲了什么"
  
  like a test in my macbook:
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

## if using Chinese, Chinese language task must lead low hit rate like that example : 
    a.js#0(0), a.js#1(0), a.js#2(0), a.js#3(0), a.js#4(0), a.js#5(0), a.js#6(0), a.js#7(0)
