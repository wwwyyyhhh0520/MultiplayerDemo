# MultiplayerDemo
photon+Unity
# 3D 多人联机射击 Demo

---

## 项目介绍
基于 **Unity 2022 LTS + Photon PUN 2** 开发的轻量 **3D 多人联机射击 Demo**，完整实现房间匹配、实时网络同步、射击战斗、**AI 机器人追击攻击**等核心功能。


---

## 核心功能
- **多人联机匹配**
  自动连接 Photon 服务器 → 自动创建/加入房间 → 支持 2–4 人实时联机
- **3D 角色控制**
  移动、跳跃、旋转、鼠标视角、Character Controller 标准实现
- **高精度网络同步**
  位置/旋转插值平滑，降低网络延迟卡顿
  自定义 `IPunObservable` 状态同步
  带宽优化，仅同步关键数据
- **射击与伤害系统**
  子弹物理发射、碰撞检测、玩家/AI 统一伤害、死亡销毁
- **AI 机器人**
  NavMesh 自动寻路
  动态搜索最近玩家
  追击 → 停止攻击 逻辑
  可被玩家击杀、死亡消失

---

## 技术栈
- 引擎：**Unity 2021.3+/2022.3 LTS**
- 网络：**Photon PUN 2**
- 语言：**C#**
- AI：**Unity NavMesh**
- 核心：网络同步、RPC、插值平滑、战斗系统

---

## 项目结构
```
Assets/
├── Scripts/
│   ├── Network/       # 网络管理、房间匹配
│   ├── Player/         # 玩家控制、血量、射击
│   ├── AI/             # AI 控制器、追击、血量
│   └── Weapon/         # 枪支、子弹、碰撞逻辑
├── Prefabs/
│   ├── Player.prefab
│   ├── AI.prefab
│   └── Bullet.prefab
└── Scenes/
    └── GameScene.unity
```


## 许可证
MIT License

---
