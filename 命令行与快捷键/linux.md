# brew

## 加速

1. 替换 / 还原 brew.git 仓库地址

1. ```cd "$(brew --repo)"
   # 替换成阿里巴巴的 brew.git 仓库地址
   git remote set-url origin https://mirrors.aliyun.com/homebrew/brew.git
   
   # 还原为官方提供的 brew.git 仓库地址
   cd "$(brew --repo)"
   git remote set-url origin https://github.com/Homebrew/brew.git
   ```

2. 替换 / 还原 homebrew-core.git 仓库地址

   ```
   # 替换成阿里巴巴的 homebrew-core.git 仓库地址
   cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
   git remote set-url origin https://mirrors.aliyun.com/homebrew/homebrew-core.git
   
   # 还原为官方提供的 homebrew-core.git 仓库地址
   cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
   git remote set-url origin https://github.com/Homebrew/homebrew-core.git
   ```

3. 替换 / 还原 homebrew-bottles 访问地址

   ```
   # 替换 homebrew-bottles 访问 URL:
   echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.aliyun.com/homebrew/homebrew-bottles' >> ~/.bash_profile
   source ~/.bash_profile
   
   # 还原为官方提供的 homebrew-bottles 访问地址
   vi ~/.bash_profile
   # 然后，删除 HOMEBREW_BOTTLE_DOMAIN 这一行配置
   source ~/.bash_profile
   ```

# jupyter

## 转换

`jupyter nbconvert --to html test.ipynb`

​	•	HTML

- LaTeX
- PDF
- Reveal JS
- Markdown (md)
- ReStructured Text (rst)
- executable script

## jupyter-themes

` -t grade3 -altp -cellw 88% -T -fs 11 -lineh 140  -tf exosans -tfs 12 -nf exosans -nfs 10 -dfs 10`



## 修改工作目录

配置地址：`jupyter notebook --generate-config`

修改：c.NotebookApp.notebook_dir = '/Users/supeeeer/Documents/myGitHub/Learning'