# pkg-mirror

`xiealon/apk` 与 `xiealon/store` 的**镜像备份**（只保留当前文件树）。

- 同步：GitHub Actions `.github/workflows/mirror.yml`（不走本机上传）
- 触发：手动 dispatch，或每天 02:00（北京）自动一次
- `SOURCES.txt`：记录每次同步时源仓库的 `HEAD` 与时间
- 不含 git 历史：两源仓历史合计 3.2 GB，会顶到单次 push 上限；本仓目的是「内容不丢」

恢复示例：

```sh
git clone https://github.com/xiealon/pkg-mirror.git
ls pkg-mirror/apk/run/x86
ls pkg-mirror/store/run/x86
```
