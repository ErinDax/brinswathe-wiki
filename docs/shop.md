# 商店

角色专属商店（`BrinShopAccess`）——在 wathe 通用商店基础上按角色定制/新增条目。

!!! note "建设中"
    已确认条目（源码提取）：

    - **傀儡师**：自毁装置（`puppeteerSelfDestruct`，价格 `BrinConfig.puppeteerSelfDestructPrice()`）——武装后傀儡脱离控制时在傀儡位置引发爆炸（3×3×3，范围内直接击杀）
    - **赎罪者**：身份提示（`penitentIdentityHint`，`penitentIdentityHintPrice`）+ 解毒剂（`penitentAntidote`，`penitentAntidotePrice`，Type.POISON）
    - **炸弹客**：炸弹（`BomberBombShopEntry`）+ 手雷重定价（`bomberGrenadePrice`）
    - **通用重定价**：各角色 `shopPrice(roleId, ShopItem.KNIFE/REVOLVER/PSYCHO_MODE)`（刀/左轮/疯魔按角色定制价格）
    - 撬锁器 50、撬棍 25（等 wathe 通用工具）
