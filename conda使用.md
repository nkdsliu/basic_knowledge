# conda创建虚拟环境
* conda config --remove-key channels -> 删除默认源（不一定需要，当前源无法访问时尝试）
* conda create -n ocr python=3.7 -> 创建虚拟环境
* conda activate 目标环境目录  或者source activate ocr -> 激活虚拟环境
* conda install pip -> 安装pip（若创建虚拟环境是指定python版本，则pip已经安装，此处无需再安装）
* pip install -r requirements.txt -> 安装requirements.txt中包
* conda deactivate 或source deactivate -> 退出虚拟环境
* conda remove -n ocr --all -> 删除虚拟环境
* pip install -i http://pypi.douban.com/simple/ --trusted-host pypi.douban.com mmcv -> 指定豆瓣源安装包
