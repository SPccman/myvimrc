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

# 遇到的一些问题
## Leaderf
当用 Leaderf 时，发现某些目录无法被找到时，可能是因为这个目录被加到版本控制工具的忽略列表中去了，如 .gitignore。Leaderf 搜索文件时不会查找这些被忽略的目录。目前没有看到有开关将其打开。并且这里记录一下它搜索文件的命令

```
rg --no-messages --files --color never  -L --hidden

```

如果改成下面的语句，就可以找到被忽略的目录及其内部的文件

```
rg --no-messages --files --color never  -L --hidden --no-ignore
```
