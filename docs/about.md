# Brin's Wathe 简介

## 基本信息

| 项 | 值 |
|---|---|
| 模组 id | `brinswathe` |
| 包名 | `cn.autoforged.brinswathe` |
| 版本 | 1.13.0（mods 文件名 BrinsWathe-1.1.3.jar）|
| 定位 | BRIN 列车整合包专属扩展（基于 wathe）|
| 源码 | `D:\下载\brin_wateh_mod-source\brin_wateh_mod-source` |

## 模块构成（源码 main 目录）

| 文件 | 职责 |
|---|---|
| `BrinRoles` | 角色注册（22+ 角色）|
| `BrinItems` | 专属物品注册 |
| `BrinShopAccess` | 角色商店接入（自毁/身份提示/解毒剂/炸弹/重定价）|
| `BrinConfig` | 配置系统（技能价格/冷却/持续、挂机、护盾等）|
| `BrinModifiers` | 词条判定 |
| `BrinSounds` | 音效注册 |
| `BrinComponents` | CCA 组件注册 |
| `BrinsWathe` | 主类（事件/mixin/命令注册）|
| `TerroristExplosion` | 恐怖分子爆炸机制 |
| `BomberBombs` | 轰炸机炸弹机制 |
| `CowboyDuel` | 牛仔决斗机制 |
| `StuntDoubleDeathTransfer` | 替身死亡转移 |
| `BoneharvesterCorpseManager` | 拾骨师尸体管理 |
| `CompensatorPassive` | 补偿者被动 |
| `AvengerWitness` | 复仇者见证 |
| `AfkKickManager` | 挂机踢出管理 |

## 依赖关系

- 依赖 **wathe**（基础角色/商店/游戏框架）
- 与 **kinswathe** 联动（如 HACKER 角色判定）

## 内容来源与许可

- 角色/机制内容整理自 **brinswathe**（MIT License，© 2026 百家）
- wathe 相关机制为描述性整理，未复制原版文本（wathe © 2024 doctor4t，All Rights Reserved）
- 本百科 © 2026 ErinDax，以 [CC BY-SA 4.0](../LICENSE) 许可发布
