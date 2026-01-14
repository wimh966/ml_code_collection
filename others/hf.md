## Release models
* Install the lfs
    * sudo apt-get update
    * sudo apt-get install git-lfs

* Prepare models in a public dir and git lfs track
    * Make a public dir 
    * Copy a list of models there by 1) vim public_file.txt. 2) xargs -a public_file.txt cp -t public/
    * git lfs track "*.pth". 

* git prepare
    * git init; git branch -m main; Note that it needs to be main branch to align with the default branch in hf repo.
    * git config --global user.email "weixiuying966@gmail.com
    * git config --global user.name "wimh966"
    * git add .; git commit -m '[ckpt]'; 

* Relate this with the hf remote repo and push
    * git remote set-url origin https://<user_name>:<token>@huggingface.co/<repo_path>
    * git branch --set-upstream-to=origin/main main
    * git config pull.rebase true
    * git pull
    * hf lfs-enable-largefiles; git push


