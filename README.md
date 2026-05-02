# The Spell Brigade Cheat Engine Table (.CT)

这是一个为《The Spell Brigade》(V1.0.2.16657) 制作的 Cheat Engine 修改表。采用 AOB 注入技术，支持动态地址抓取，能够自动追踪并修改当前选中角色的等级和经验进度。

## 核心功能 (Features)

- **[AOB] Character Data Tracker**: 自动拦截并抓取当前查看角色的内存基址。
- **Current Rank Modifier**: 修改当前选中英雄的等级 (Offset +10)。
- **XP Progress Modifier**: 修改当前等级的经验百分比 (Offset +14)。
- **Version Independent**: 由于使用了特征码搜索 (AOB Scan)，脚本在游戏小版本更新后仍有较大几率保持有效。

## 使用要求 (Requirements)

- **Cheat Engine 7.5** 或更高版本。

## 使用方法 (How to use)

1. 启动游戏并进入主菜单。
2. 运行 Cheat Engine 并附加到游戏进程 `TheSpellBrigade.exe`。
3. 加载此 `.ct` 文件。
4. **激活脚本**：点击第一行**[Script] Rank & XP Tracker**脚本前的方框。
5. **抓取数据**：在游戏内点击进入“巫师”菜单，选中(高亮)你想修改的巫师。
6. **进行修改**：此时下方的两个地址会显示该巫师的数值。可以双击右边的vlaue下具体数值,将**Current character_rank**改为1-9中任意数字(对应游戏内等级),将**Current character_progress**改为 `0.99`(指当前这一级经验占升级所需的比例)，然后回游戏获得所需数量经验即可触发升级。

## 已知问题 (Known Issues)

- **UI 显示同步 (Visual Sync)**：由于游戏采用共享代码处理 UI 显示，当你在某个角色高亮时使用脚本，其他角色的 UI 界面也可能暂时显示为相同的数值。这只是视觉上的 Bug，实际存档数据仅在你高亮并修改的角色上生效。
- **建议**：修改成功并触发游戏自动存档后即可关闭脚本。

## 注意事项 (Disclaimer)

- **功能限定**：本项目只用于修改角色局外成长,局内数值请寻找其他修改器,为了保证数据安全,尽量不要与其他修改器同时运行.
- **合理操作**：请不要将等级或升级进度调整为不合理的数字,相关后果自行承担.
- **备份存档**：修改局外成长数据涉及存档改动，建议在操作前备份游戏存档。
- **仅限离线使用**：本工具仅供学习和个人娱乐使用，请勿在公开联机模式下使用，以免造成同步错误或影响他人游戏体验。
- **风险自担**：作者不对因使用本工具造成的存档损坏或账号问题负责。

---

**Author**: enchanter  
**Last Updated**: 2026-5-2
