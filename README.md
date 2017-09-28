# require
* running dockerlize omms env
* cubeadev

# pre-commit
本项目是git pre-commit钩子的 repo，有以下几种钩子：
* docker-pylint
* docker-eslint
* docker-es-import-sort
* docker-stylelint
* docker-python-isort
* python-isort
* python-pylint

# 使用说明
1. 使用cubeadev config配置业绩大师的地址会自动安装pre-commit钩子到本地omms项目
2. 在项目根目录添加.pre-commit-config.yaml文件来配置使用的钩子
	例如：
		repo: https://github.com/CubeADGroup/pre-commit.git
 			sha: a02c263c9a792549f69f0a6a057423a9a3a0cc5e
 	 		hooks:
    	    	- id: docker-pylint
   	 	    	- id: docker-eslint
    	    	- id: docker-stylelint
    	    	- id: docker-python-isort
    	    	- id: docker-es-import-sort

3. 若想对某些js文件跳过es-import-sort更改，可以使用在文件内添加/* eslint sort-imports:0 */来跳过该文件。
