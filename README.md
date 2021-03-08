# 配置 amix/vimrc
https://github.com/amix/vimrc
按照流程进行配置

# vim-plug
下载该插件到 /path/to/vim_runtime/autoload

# 插件初始化
## coc
1. install nodejs
2. :CocInstall coc-json coc-tsserver // vim 命令
3. coc-settings.json
```
 {
     "languageserver": {
         "ccls": {
             "command": "ccls",
             "filetypes": [
                 "c",
                 "cc",
                 "cpp",
                 "objc",
                 "objcpp"
             ],
             "rootPatterns": [
                 ".ccls",
                 "compile_commands.json",
                 ".vim/",
                 ".git/",
                 ".hg/"
             ],
             "initializationOptions": {
                 "cache": {
                     "directory": "/tmp/ccls"
                 }
             }
         }
     },
     "diagnostic.displayByAle": true,
 
 }
```
