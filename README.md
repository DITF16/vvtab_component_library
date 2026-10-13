# vvtab component library

组件库按 `packages/<组件名>/<尺寸>/<样式 ID>.json` 分类。每个文件包含当前尺寸的 CSS 和运行代码，且仅对应这一款样式；皮肤与样式统一称为“样式”。`catalog.json` 列出可用的尺寸、样式、文件路径及 SHA-256 哈希。

更新时只需修改对应的 JSON，再从 vvtab 主仓库执行 `node scripts/publish-widgets.js <本仓库路径>` 重新生成目录哈希。客户端按所选尺寸/样式下载、校验、预览和安装，更新一个文件不会覆盖同组件其他尺寸或样式。新增样式也必须在文件中填写匹配的组件 ID、尺寸、样式 ID、名称、CSS、代码及空权限列表。
