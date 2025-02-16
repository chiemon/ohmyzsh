
## 克隆到本地

git clone --recursive https://github.com/chiemon/ohmyzsh.git $HOME/.oh-my-zsh

## 版本要求

| plugins                 | zsh                              |
| ----------------------- | -------------------------------- |
| zsh-syntax-highlighting | ≥ 4.3.11                         |
| zsh-autosuggestions     | ≥ 4.3.11                         |
| zsh-autocomplete        | ≥ 5.8(tested) 、5.4(should work) |

## 配置文件

1. 创建 .zshrc.d 目录

    ```bash
    mkdir ~/.zshrc.d
    ```

2. 将原 .zshrc 位置文件移动到 .zshrc.d 目录下

    ```bash
    mv ~/.zshrc ~/.zshrc.d/default.zshrc
    ```

3. 创建新的 ~/.zshrc 文件

    ```bash
    touch ~/.zshrc
    ```

4. 修改配置文件：

    - **~/.zshrc**

        ```bash
        if [ -d ~/.zshrc.d ]; then
        for i in ~/.zshrc.d/*.zshrc; do
            if [ -r $i ]; then
            . $i
            fi
        done
        unset i
        fi 
        ```

    - **~/.zshrc.d/default.zshrc**

        ```bash
        ZSH_THEME="powerlevel10k/powerlevel10k"


        plugins=(
            git
            zsh-proxy
            zsh-syntax-highlighting
            zsh-autosuggestions
            zsh-autocomplete
        )
        ```

## 插件

### powerlevel10k

```bash
p10k configure
# Does this look like a diamond (rotated square)?     y        diamond(钻石)
#
# Does this look like a lock?                         n
# Let's try another one. Does this look like a lock?  n
# Prompt Style                                        4(Pure)
# Prompt Colors                                       1(Original.)
# Non-permanent content location                      2(Right)
# Show current time?                                  2(24-hour format)
# Prompt Height                                       2(Two lines)
# Prompt Spacing                                      2(Sparse)
# Enable Transient Prompt?                            n(No)
# Instant Prompt Mode                                 1(Verbose)
```

### zsh-proxy

```bash
# 初始化
init_proxy

# 配置
config_proxy
# [socks5 proxy] {Default as 127.0.0.1:1080}
# (address:port):                                                                               192.168.6.253:7890
# [socks5 type] Select the proxy type you want to use {Default as socks5}:
# 1. socks5
# 2. socks5h (resolve DNS through the proxy server)
# (1 or 2):                                                                                     1
# [http proxy]   {Default as 127.0.0.1:8080}
# (address:port):                                                                               192.168.6.253:7890
# [no proxy domain] {Default as 'localhost,127.0.0.1,localaddress,.localdomain.com'}
# (comma separate domains): 
# [git proxy type] {Default as socks5}
# (socks5 or http):                                                                             http

# 启用代理
proxy

# 禁用代理
noproxy

# 查看正在使用的 IP
myip
```