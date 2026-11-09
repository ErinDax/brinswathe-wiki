# 配置

配置文件：**`config/brinswathe.json5`**（旧版 `brinswathe.json` 会在首次启动时自动迁移）。
配置类：`cn.erindax.brinswathe.config.BrinConfig`，当前 `config_version = 48`（版本低于当前的旧配置会自动迁移新的默认值）。

修改后可用 `/brinswathe reload` 在游戏内热重载，无需重启服务器。

## 文件结构

```json5
{
  config_version: 48,
  announcement: [],
  afk_kick: { enabled: true, idle_seconds: 60, countdown_seconds: 60 },
  harpy: {
    neutral_role_count: ...,
    killer_role_count: ...,
    vigilante_role_count: ...,
    role_modifier_blacklist: { ... }
  },
  roles: {
    <roleId>: {
      skill_cost: ...,
      skill_cooldown_seconds: ...,
      skill_duration_seconds: ...,
      shop_prices: { knife: ..., revolver: ..., psycho_mode: ... }
      // 部分角色还有专属字段
    }
  }
}
```

## 全局配置

| 配置项 | 说明 | 默认 |
|---|---|---|
| `afk_kick.enabled` | 是否开启挂机处死 | `true` |
| `afk_kick.idle_seconds` | 判定挂机的静止秒数 | 60 |
| `afk_kick.countdown_seconds` | 处死前的倒计时秒数 | 60 |
| `harpy.neutral_role_count` | 中立角色数量 | 见 Harpy 分配 |
| `harpy.killer_role_count` | 杀手角色数量 | 见 Harpy 分配 |
| `harpy.vigilante_role_count` | 义警角色数量 | 见 Harpy 分配 |
| `harpy.role_modifier_blacklist` | 职业特质黑名单（`/rolemodifierblacklist` 管理） | `{}` |

## 角色默认值（`roles.<roleId>`）

`商店价格` 依次为 **刀 / 左轮 / 疯魔**。

| 角色 | `skill_cost` | 冷却 | 持续 | 商店价格 | 专属字段 |
|---|---|---|---|---|---|
| 傀儡师 `puppeteer` | 0 | 200 | 60 | 150 / 300 / 300 | `self_destruct_price` 350、`return_cooldown_seconds` 60、`particle_delay_seconds` 45 |
| 替身演员 `stunt_double` | 0 | 30 | 30 | 100 / 350 / 300 | — |
| 灵媒 `medium` | 200 | 120 | 8 | 100 / 500 / 300 | — |
| 合谋者 `conspirator` | 150 | 200 | 15 | 100 / 350 / 300 | — |
| 生存专家 `watchman` | 150 | 30 | — | 100 / 350 / 300 | — |
| 捕兽者 `beast_trapper` | 25 | 120 | — | 100 / 300 / 300 | `trap_limit` 1、`extra_trap_price` 150、`trap_catch_reward` 50 |
| 梦魇 `nightmare` | 0 | 60 | 0 | 100 / 300 / 300 | `forced_sleep_task_cooldown_seconds` 200 |
| 幻术师 `illusionist` | 0 | 120 | 10 | 100 / 300 / 300 | — |
| 狙击手 `sniper` | 0 | 100000 | — | 150 / 225 / 300 | `sniper_kills_to_reset` -1、`glow_seconds` 10、`sniper_tasks_to_reset` 20 |
| 狂战士 `berserker` | 0 | 0 | 0 | 100 / 300 / 800 | — |
| 档案员 `archivist` | 125 | 30 | — | 100 / 350 / 300 | — |
| 复仇者 `avenger` | 0 | 0 | 20 | 100 / 350 / 300 | `instinct_seconds` 6 |
| 变态 `stalker` | 0 | 90 | — | 100 / 350 / 300 | — |
| 牛仔 `cowboy` | 500 | 0 | — | 100 / 350 / 300 | `duel_timeout_seconds` 90、`duel_countdown_seconds` 3、`duel_music_volume` 100 |
| 瓦伦西娜 `valentina` | 0 | 0 | 10 | 100 / 350 / 300 | — |
| 安检员 `inspector` | 200 | 0 | 10 | 100 / 350 / 300 | — |
| 拾骨师 `boneharvester` | 0 | 0 | — | 100 / 300 / 300 | `bone_knife_price` 175、`bone_knife_cooldown_seconds` 200 |
| 炸弹客 `bomber` | 0 | 0 | — | 100 / 300 / 300 | `grenade_price` 200、`bomb_price` 75、`mine_price` 125、`bomb_fuse_seconds` 45、`bomb_warning_seconds` 30、`bomb_explosion_size` 2、`mine_stun_seconds` 3、`bomb_purchase_cooldown_seconds` 60 |
| 代偿者 `compensator` | 0 | 0 | 0 | 100 / 300 / 300 | — |
| 赌徒 `gambler` | 100 | 0 | 0 | 100 / 300 / 300 | — |
| 赎罪者 `penitent` | 0 | 0 | — | 100 / 300 / 300 | `identity_hint_price` 150、`antidote_price` 100、`starting_shield_layers` 0 |
| 恐怖分子 `terrorist` | 0 | 0 | 0 | 100 / 300 / 300 | `explosion_range` 5、`explosion_survival_kills` 4、`revolver_shop_enabled` false |
| 入殓师 `mortician` | 0 | 100 | 5 | 100 / 300 / 300 | — |
| 张师 `zhangshi` | 0 | 90 | 10 | 100 / 300 / 300 | `xuezi_price` 150、`xuezi_cooldown_seconds` 200、`xuezi_shield_layers` 1、`run_speed` 2.0 |

> 说明：表中「—」表示该角色无此配置项；狙击手冷却 100000 为「开局不可用」的实现方式（需完成任务恢复）。

## 相关指令

| 指令 | 说明 |
|---|---|
| `/brinswathe reload` | 热重载配置 |
| `/brinswathe setconfig <字段> <值>` | 游戏内直接改配置 |
| `/setbrinspeed <玩家> <类型> <数值>` | 调整体力与奔跑参数 |
| `/setrolecount` | 设置各阵营角色数量 |
| `/rolemodifierblacklist` | 管理职业特质黑名单 |
