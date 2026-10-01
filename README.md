# Helldivers-2-steamUrlButton-untest-V1
One-click open a teammate's Steam profile from the ESC squad menu mod for Helldivers 2

steamUrlButton

在 ESC 小队菜单里，一键打开队友的 Steam 个人主页。

按下 ESC，再按 F7，每名队员右侧会显示一个 [Profile] 按钮。点击即可在 Steam 叠加浏览器里打开该玩家的 Steam 主页。

依赖
Bingus Shared Loader v15 或更新

使用

打开按钮
- 进入游戏（主菜单 / 船上 / 任务中均可）。
- 按 ESC 打开小队菜单。
- 按 F7 -> 每名队员右侧出现 [Profile]。
- 首次按 F7 会触发一次内存扫描（约 6-15 秒）。期间右上显示 Scanning players...，4 行按钮全部灰色。
- 扫描完成后，有 Steam 数据的玩家 [Profile] 亮起。

点击按钮
- 亮着的 [Profile] -> 点击后 Steam 叠加层自动打开，跳到该玩家的个人主页。
- 灰色的 [Profile] -> 该玩家尚未扫描到 Steam 数据，不可点击。

关闭按钮
- 再按一次 F7 -> 按钮消失。
- 或者直接关闭 ESC 菜单 -> 按钮自动消失。

热键
F7：打开 / 关闭 [Profile] 按钮。条件：需 ESC 菜单打开。
F6：重新扫描当前局的玩家。条件：任何时刻，不需要 ESC。

F6 重扫
- 中途有玩家加入：新行 [Profile] 是灰色。按 F6 重扫 -> 变亮。
- 中途有玩家退出：旧行 [Profile] 亮着但点了会失败。按 F6 重扫 -> 变灰。
- 一切正常：不需要按。

警告
一次扫描约 15 秒（根据你本机实际情况来）。不要狂按 F6——扫描进行中再按会被忽略，但连按会给游戏增加读取压力。

常见问题
- 按 F7 无反应
  原因：(1) ESC 菜单没打开；(2) loader 版本太旧。
  处理：先开 ESC 再按；检查 loader 版本。
- 一直显示 Scanning
  原因：正在扫，正常。
  处理：等 15 秒。
- 某人 [Profile] 灰
  原因：刚加入，或映射还没扫到。
  处理：按 F6 重扫。
- 点击 [Profile] 后，浏览器没开
  原因：Steam 客户端没运行 / 叠加层被禁用。
  处理：检查 Steam 设置里“游戏内叠加”是否开启。
- 完全没日志
  原因：mod 没被加载。
  处理：查 BingusSharedLoader.log 里 mods/codex/stingray_probe 是否为 loaded。
- 装了没效果
  原因：Deploy 没生效。
  处理：管理器里重新 Deploy 一次。

行为说明
- mod 仅读取游戏内存。
- 无内存修改、无外部进程：纯查询 + 打开浏览器。
- 本地：所有数据只存在于内存中，不写文件、不上传网络。
- 跨平台玩家无 Steam 主页：PSN / Xbox 玩家没有 Steam64 ID，对应行 [Profile] 会保持灰色。
- 同一局扫描一次：中途有玩家变动需要手动按 F6，不会自动重扫。

steamUrlButton (untest) V1

感谢各方开源，其做法和调用给我很多灵感
感谢DS

