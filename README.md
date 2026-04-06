# ansible-init-project
Ansible playbook for new server initialization
# 服务器自动化初始化工具

## 项目简介
编写 Ansible Playbook，实现新服务器的“一键初始化”。

## 技术栈
- Ansible
- Shell

## 项目成果
- 将新服务器上线准备时间从 **1 小时缩短到 5 分钟**
- 配置标准化，避免人工操作失误

## 实现的功能
- 创建 deploy 用户并配置 sudo 权限
- 修改 SSH 端口（22 → 2222），禁止 root 登录
- 安装常用软件包（vim, net-tools, htop）
- 配置时间同步（chrony）

## 文件说明
- `init_server.yml` - 主 Playbook
- `hosts.ini` - 主机清单

## 使用方法
```bash
ansible-playbook -i hosts.ini init_server.yml
