# u-open-imla

## 维吾尔语校对词汇基库

uyghur tili imla sozlvk ambiri

--- 

### 项目地址

> 我们更多的讨论希望都在github上进行，
> 由于Hub的issue无法同步到gitee，望你发起讨论时优先在hub上开启issue

- [国内 Gitee](https://gitee.com/silvaq/u-open-imla)

- [GitHub](https://github.com/ishirkhan/u-open-imla)

---

## 目前的词汇情况

- 总语料词汇 ` 203,516 `
- 标准词汇 ` 421,110 `
- 推荐词  ` 19,397 `
- 本项目禁用词 ` 2204 + 198 `

---

# 声明

- 本项目是免费的开源项目，所有成果可在 MIT 所允许的范围内使用在符合法律法规的产品上
- 严禁将本项目的成果用于非法用途或以个人名义传播
- 本项目中的所有判定及结论属于本项目的维护者，不代表任何组织机构，更不代表任何法律法规内容，严禁虚假用途。
- 本项目是为了帮助和促进更多的符合国家法律法并有利于少数民族语言发展的产品，严禁私下交易和非法传播。

> 如果你发现任何不符合法律法规的行为或者问题，请及时和我们联系，或者公开指出问题，我们会以最快的速度处理

# 注意

- 本项目code中的 shirkhan python lib 从本项目中分离，单独存放在 shirkhan_pylib项目中
  > 更多信息请看本文档的  [相关开源项目部分](https://github.com/SilvaQ/shirkhan_pylib?#%E7%9B%B8%E5%85%B3%E5%BC%80%E6%BA%90%E9%A1%B9%E7%9B%AE)

## todo list

- [ ] 生成词缀库[前缀，中缀，后缀]

## finished list

- [x] 所有标准库清洗并扩充先有标准库
- [x] 新增维吾尔语词汇分音节功能
- [x] 处理合并语料 v5_20210222154849.txt 生成标准词汇和推荐词 [20210222154849]
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

---

# 相关开源项目

- [shirkhan python library](https://github.com/SilvaQ/shirkhan_pylib)
- [uyghur Spell Check](https://github.com/gheyret/UyghurEditPP)

# 常用 shell 命令

统计 corpus 中各个文件 和行数

```shell
 ls ./corpus/sources/**/*.txt|xargs -n 1 -I {} wc -l {}
```

统计总 corpus 行数

```shell
ls ./corpus/sources/**/*.txt|xargs -n 1 -I {} wc -l {}|awk -F " "  '{sum += $1} END {print sum}'
```