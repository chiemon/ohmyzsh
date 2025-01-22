
## .zshrc

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

## powerlevel10k

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

## zsh-proxy

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