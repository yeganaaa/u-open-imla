# u-open-imla

## 维吾尔语校对词汇基库

uyghur tili imla sozlvk ambiri

## 目前的词汇情况

- 总语料词汇 ` 183,902 `
- 标准词汇 ` 102,308 `
- 推荐词  ` 16,149 `

---

## 我们需要你

- [ ] 我们需要更多比较有名公众号，网站或者其他媒体的文本内容，用来做过滤词和其他扩展功能的研发，你能帮助我们整理
  > 数据格式目前没有严格要求，纯文本内容最好,word,excel也可以。
  > 网站类内容 可以直接ctl+s 存档。脚本程序能够去掉不相关信息保留需要的母语词汇，所以尽量保存，不用纠结内容中的无相关内容

- [ ] 原料词汇中存在一些根本不算词汇，没有意义的行 如：A，e,me 等，需要找到规律删除这些干扰信息
- [ ] 程序可能存在代码质量或者性能等问题，需要完善，调优
- [ ] 部分逻辑可能存在风险，bug，需要修复，扩展
- 其他需要帮忙的内容即将继续补充

## todo list

- [ ] 继续找靠谱语料数据，继续扩展 imla_core 词汇


## finished list

- [x] 处理合并语料 v4_20210220140620.txt 生成标准词汇和推荐词 [v4_20210220140620]
- [x] 处理合并语料 v3_20210220104002.txt 生成标准词汇和推荐词 [20210220104002]
- [x] 处理合并语料 v2_20210219174227.txt 生成标准词汇和推荐词 [20210219174227]
- [x] 基于 v1_20210219144221.txt 生成推荐词词库 [20210219144221]
- [x] 用现在积累的语料词汇集生成校对过的有效 imla 词汇集 [20210219144221]
- [x] 提取 shirkhan 公众号的历史帖子中的词汇，生成原料词汇
- [x] 提取 fyj_ad1 中的词汇，生成原料词汇
- [x] 提取 txw 中的词汇，生成原料词汇
- [x] 提取 idris_java 书中的词汇，生成原料词汇
- [x] 脚本集做成 library，方便使用、扩展、维护、更新
- [x] 准备纯文本中提取内容脚本

# 常用 shell 命令

统计 corpus 中各个文件 和行数

```shell
 ls ./corpus/sources/**/*.txt|xargs -n 1 -I {} wc -l {}
```

统计总 corpus 行数

```shell
ls ./corpus/sources/**/*.txt|xargs -n 1 -I {} wc -l {}|awk -F " "  '{sum += $1} END {print sum}'
```