## itrashcan 一个简易的Linux回收站
1. 在`~/.bashrc`中粘贴下面的设置环境变量, 并执行`source ~/.bashrc`, 或者重新打开终端
    ```
    # itrashcan
    export itrashcan="/home/szw/repos/itrashcan" # set the script path
    export itrashcan_home="/home/szw/.trashcan" # set the transcan path
    source "$itrashcan/config.sh" # source the config for alias
    ```
2. 初始化itrashcan
    ```
    bash $itrashcan/init.sh
    ```
3. 查看config.sh中的命令别名
    ```
    # rm by itrashcan
    alias rm="$itrashcan/delete.sh"

    # clear the trashcan
    alias rc="$itrashcan/clear.sh"

    # restore the target
    alias re="$itrashcan/restore.sh"

    # go to the trashcan
    alias gor="cd $itrashcan_home/trash"

    # get the size of trashcan
    alias rsize="du -sh $itrashcan_home/trash"
    ```
4. remove the itrashcan
    ```
    bash remove.sh
    ```
