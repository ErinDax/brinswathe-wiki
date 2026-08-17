# 核心机制

!!! note "建设中"
    已确认机制（源码文件提取）：

    | 机制 | 源码 | 说明 |
    |---|---|---|
    | 傀儡控制 | `PuppeteerControlComponent` / `PuppetEntity` | 傀儡师操控傀儡（`PuppetEntity`），本体在傀儡上方；傀儡受击仅解除操控，替身受击=傀儡师真死 |
    | 傀儡自毁 | `selfDestruct` | 购买自毁武装后，傀儡脱离控制时爆炸：**3×3×3 范围（±1.5 格）内玩家直接击杀**（死因 GRENADE）|
    | 恐怖分子爆炸 | `TerroristExplosion` | 被枪杀时引发爆炸；爆炸消灭足够玩家则存活；爆炸中恐怖分子连锁爆炸 |
    | 炸弹客 | `BomberBombs` | 地雷/贴人炸弹（`bomberBombExplosionSize`）|
    | 牛仔决斗 | `CowboyDuel` | 背对背各一把左轮，一局限用一次 |
    | 替身转移 | `StuntDoubleDeathTransfer` | 替身演员代替模仿对象承受致命伤害 |
    | 拾骨师 | `BoneharvesterCorpseManager` | 击杀后隐藏尸体，死者片刻后显现 |
    | 代偿者 | `CompensatorPassive` | 以命换命，击杀者自食其果 |
    | 复仇者 | `AvengerWitness` | 目睹击杀后短暂获得左轮+本能 |
    | 挂机踢出 | `AfkKickManager` | 按配置自动踢出挂机玩家 |
