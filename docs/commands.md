# 命令

## 配置类（`/brinswathe`）

| 指令 | 说明 |
|---|---|
| `/brinswathe reload` | 在游戏内直接应用配置、语言、皮肤白名单与皮肤，无需重启服务器 |
| `/brinswathe afk on` | 开启游戏内挂机处死功能 |
| `/brinswathe afk off` | 关闭游戏内挂机处死功能 |
| `/brinswathe setconfig <字段> <值>` | 直接修改配置项（等价于编辑 `brinswathe.json5` 后 reload） |
| `/brinswathe gui` | 打开管理设置界面（需要客户端安装最新版模组） |

## 体力与奔跑

`/setbrinspeed <玩家> <类型> <数值>`

| 类型 | 说明 |
|---|---|
| `maxStamina` | 最大体力（范围 1–1000，默认 150）|
| `runSpeed` | 奔跑速度倍率（范围 0.0–10.0，默认 0.1）|
| `regenRate` | 体力回复速度（范围 0–100，默认每秒 2）|

不带目标时可恢复全局体力设置为默认值。

## 角色分配

### `/setrolecount <类型> <数值>`

设置各阵营角色数量，支持三种模式：

- **原版默认**
- **固定数量**
- **动态**（每 N 名玩家分配 1 个）

类型：`neutral`（中立）、`killer`（杀手）、`vigilante`（义警）

### `/forcerefreshrole`

| 用法 | 说明 |
|---|---|
| `add <职业>` | 设置某职业必定在后续分配中刷新至少 1 次 |
| `remove <职业>` | 从强制刷新列表中移除 |
| `list` | 查看当前强制刷新职业列表 |
| `clear` | 清空强制刷新职业列表 |

### `/rolemodifierblacklist`

| 用法 | 说明 |
|---|---|
| `add <职业> <特质>` | 将特质加入该职业的黑名单 |
| `delete <职业> <特质>` | 从黑名单中移除 |
| `list` | 查看职业特质黑名单配置 |

## 玩家指令

| 指令 | 说明 |
|---|---|
| `/iWantBe` | 自选职业（场上 Initiate 多于 1 人时不可用）|
| `/killme` | 自杀（可被管理员禁用）|

## 其他管理指令

以下指令由管理员使用，可在游戏内用 Tab 补全查看完整参数：

`/draft`（轮抽选角）、`/secretmurder`、`/musicbox`（结算音乐盒）、`/planb`（惩罚名单）、`/weights`（角色权重）、`/roleRoundsclear`（清空轮次权重与防连任记录）、`/hudnames`、`/nv`（夜视）、`/allergic`（过敏类型）、`/armor`、`/food`、`/drink`、`/psycho`（疯魔）、`/km`、`/setcd`（设置冷却）、`/setRecover`、`/setMaxSprintingTicks`、`/setMinSprintingTicks`、`/setnow`、`/setplayer`、`/remark`（玩家备注）、`/PrintRounds`

> 皮肤与音乐盒的上传/删除等操作在 `/brinswathe` 下的子命令中（如 `skin`、`upload`、`delete`、`files`），具体参数以游戏内 Tab 补全为准。
