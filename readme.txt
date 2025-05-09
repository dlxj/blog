
see nodejs summary.md -> 范畴论 -> Go Monads -> ugo blog

see https://github.com/MathAgape/blog



安装 winget 

    https://github.com/microsoft/winget-cli/releases/download/v1.11.230-preview/Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.msixbundle

win11 + PowerShell 7

    $PSVersionTable.PSVersion
        # ps 版本默认是5

    winget search Microsoft.PowerShell
        --> 7.5.1.0

    winget install --id Microsoft.PowerShell --version 7.5.1.0 --source winget

     Test-Path "C:\Program Files\PowerShell\7\pwsh.exe"
        # 装到这里了

     > & "C:\Program Files\PowerShell\7\pwsh.exe"
        --> PowerShell 7.5.1
            # 成功运行新版 ps
            # 但是默认打开的还是旧版 ps

    C:\Program Files\PowerShell\7
        # 环境变量的 path 把这条移到最上面
        # win 键 -> 搜 powershell 能看见 ps7（深蓝色图标）


安装 Hugo

	winget install Hugo.Hugo.Extended

	PowerShell hugo version
		--> hugo v0.147.1


Mainroad 主题选这个

    hugo new site blog
    cd  blog
    git init
    git submodule add https://github.com/MathAgape/Mainroad.git
    	# https://github.com/vimux/mainroad.git themes/mainroad
    echo "theme = 'mainroad'" >> hugo.toml
    hugo server
    	# http://localhost:1313/


	blog\.gitmodules
        [submodule "themes/mainroad"]
        path = themes/mainroad
        url = https://github.com/MathAgape/Mainroad.git
	git submodule update --remote -- themes/mainroad
		# 这样更新主题

    hugo new content content/posts/my-first-post.md
        # 新建文章

    用编辑器打开 my-first-post.md（我使用 VS Code 编辑器），会发现一些以 +++ 包围的内容，称为 Front Matter 。

    在 Front Matter 中，注意到 draft = true。这意味着该文档为草稿状态，使用 hugo server 命令无法看到这篇文档，而要使用以下命令才能预览到草稿：

    hugo server -D


git clone https://github.com/dlxj/blog
	# https://github.com/MathAgape/blog 从这里 clone 来的


https://dlxj.github.io/blog
	# https://mathagape.github.io/blog
	# blog 访问地址



