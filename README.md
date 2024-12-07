<div align="center">

# maimaiDX-songs

_✨ 舞萌DX歌曲数据库 ✨_

</div>

---

## 数据结构

<details>
<summary>version</summary>

## 更新日期

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| data | int | data的更新日期 |
| songs | int | song的更新日期 |
| alias | int | alias的更新日期 |
| flevel | int | flevel的更新日期 |
</details>

<details>
<summary>metadata</summary>

## 通用数据

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| genre | object | 乐曲分类 |
| version | object | 乐曲版本 |
| type | object | 乐曲类型 |
| diff | object | 乐曲难度 |

### genre

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| id | int | 分类id |
| jp | str | 日服分类名称 |
| cn | str | 国服分类名称 |
| intl | str | 国际服分类名称 |
| color | str | 分类颜色代码 |

### version

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| id | int | 版本id |
| version | str | 版本名称 |
| cn | str | 国服名称 |
| abbr | str | 版本代号 |

### type

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| id | int | 类型id |
| type | str | 类型代码 |
| name | str | 类型名称 |
| range | array | 类型范围 |

### diff

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| id | int | 难度id |
| name | str | 难度名称 |
| color | str | 难度颜色代码 |

</details>


<details>
<summary>songs</summary>

## 乐曲数据

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| id | int | 谱面id |
| type | int | 谱面类型 |
| name | str | 乐曲名称 |
| artist | str | 艺术家 |
| dimg | str | 乐曲图片(dxdata) |
| nimg | str | 乐曲图片(maimainet) |
| bpm | int | BPM |
| genre | int | 乐曲分类 |
| version | int | 追加版本 |
| date | str | 追加日期 |
| regions | object | 可用地区 |
| charts | array | 谱面信息 |
| overrides | object | 信息覆写 |

### regions

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| jp | bool | 日服解锁情况 |
| intl | bool | 国服解锁情况 |
| cn | bool | 国服解锁情况 |

## charts

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| level | float | 难度定数 |
| charter | str | 谱师 |
| notes | array | 音符信息 |
| levelHistory | array | 定数历史记录 |

### notes
| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| notes[0] | int | tap音符数量 |
| notes[1] | int | hold音符数量 |
| notes[2] | int | slide音符数量 |
| notes[3] | int | break音符数量 |
| notes[4] | int | touch音符数量 |

### levelHistory

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| 版本id | int | 难度定数 |

</details>


<details>
<summary>songs_cn</summary>

## 国服数据

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| id | int | 谱面id |
| name | str | 乐曲名称 |
| date | str | 追加日期 |
| ver | int | 追加版本 |

</details>


<details>
<summary>alias</summary>

## 乐曲别名

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| name | str | 乐曲名称 |
| alias | array | 别名列表 |

</details>


<details>
<summary>flevel</summary>

## 拟合定数

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| name | str | 乐曲名称 |
| type | int | 谱面类型 |
| flevel | array | 拟合定数 |

</details>


<details>
<summary>tags</summary>

## 乐曲标签

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| name | str | 乐曲名称 |
| type | int | 谱面类型 |
| tag | object | 乐曲标签列表 |

### tag

| 字段名 | 类型 | 说明 |
| --- | --- | --- |
| 难度id | array | 乐曲标签 |

</details>


## 数据来源
- [dxrating](https://github.com/gekichumai/dxrating)
- [diving-fish](https://www.diving-fish.com/maimaidx/prober)
- [Yuri-YuzuChaN](https://github.com/Yuri-YuzuChaN/maimaiDX)
- [MaimaiData](https://github.com/PaperPig/MaimaiData)
