# 点击长安：哪座寺庙在你脚下

这是一个展示唐代长安佛寺时空分布的静态网页项目。页面结合长安坊里地图、寺庙点位、寺庙类型筛选、坊名/功能区底图切换和时间轴交互，用于观察唐代长安寺庙在空间和时间上的分布特征。

在线访问：

https://neuracal.github.io/Temples-of-Tang/

## 功能

- 在长安地图上查看寺庙空间分布。
- 按寺庙类型筛选点位，包括僧寺、尼寺、皇家寺庙、舍宅为寺等。
- 切换不同地图底图：空白地图、坊名地图、坊功能区地图。
- 查看存在寺庙的坊列表。
- 查看寺庙类型统计表。
- 使用时间轴观察寺庙数据随时间的变化。

## 项目结构

```text
.
├── index.html              # 网页入口
├── css/                    # 页面样式和 Leaflet 样式
├── js/                     # 页面交互逻辑、D3、Leaflet
├── data/                   # 寺庙、坊里、统计数据 JSON
├── image/                  # 地图、图标、背景图等资源
└── README.md
```

## 本地运行

这个项目是纯静态网页，不需要 React、Vite 或 npm 构建。由于页面会读取本地 JSON 数据，建议通过本地服务器打开，不要直接双击 `index.html`。

进入项目目录：

```powershell
cd D:\Interest\temple
```

启动本地服务器：

```powershell
python -m http.server 8000
```

然后在浏览器打开：

```text
http://127.0.0.1:8000/
```

如果 `python` 命令不可用，可以尝试：

```powershell
py -m http.server 8000
```

停止服务器时，在终端按：

```text
Ctrl + C
```

## 数据与资源

- `data/temples.json`：寺庙数据。
- `data/neighborhood.json`：坊里相关数据。
- `data/neighborhood-temple-count.json`：坊里寺庙数量统计。
- `image/blank-map.svg`：空白底图。
- `image/neighborhood-name-map.svg`：坊名底图。
- `image/function-map.svg`：坊功能区底图。

## 技术

- HTML / CSS / JavaScript
- D3.js
- Leaflet
