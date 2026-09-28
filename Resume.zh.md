[English](./Resume.en.md)

# 洪伟  Wally Hung

16 年大数据与实时架构  |  心动科技 · TapTap  ·  大数据开发工程师  ·  2023.05 – 至今
177-4081-7241  ·  hongwei200612@gmail.com
三峡大学 · 信息与计算科学 · 理学学士 · 2006.09 – 2010.06

## 职业摘要

16 年大数据与实时计算。前 12 年以开源自建为主：Hadoop / Hive / Spark / Flink / Kafka / Elasticsearch / Kubernetes——唯品会做过 800+ 节点 Hadoop 引擎（源码调优、版本升级与热升级）；拼多多基于 Flink 1.5 / 1.8 做核心引擎研发、性能调优与热重启，并在 15k node 上把 Flink on K8s 做成平台；声网自研 Flink 发行版（merge 社区 900+ patch）。近 3.5 年在心动 TapTap 把同一套能力落到阿里云 DataWorks / MaxCompute / EMR Spark / DLF / Hologres，做成游戏广告、推荐、ADN 与训练的业务结果。能在开源栈和云托管栈之间做选型、迁移、双跑与成本对照，并把线上经验编码为 Agent Skills / Harness。

## 关键结果

- **+2,000 万**：首页广告实时特征，保守年增收
- **CPM +5%**：iOS 实时特征补齐后的核心指标
- **成本 -75%~80%**：ADN 实时链路月度成本下降
- **3.7 → 2.8 PB**：DLF 存储治理，小文件 650 万 → 160 万
- **2,000 万 QPS**：声网 Spark routing → Flink 迁移峰值
- **60 天 → 1 天**：声网混合云资源交付周期

## 专业能力

- **开源计算与存储**：Flink 1.5 / 1.8 引擎研发、调优与热重启 / Hadoop 引擎：MR / Hive / HDFS / YARN 源码级调优 / Flink on YARN / Kubernetes 平台化 / Hudi / Paimon 湖仓表格式
- **实时采集与检索**：Kafka / Flume / Logstash 开发调优 / Elasticsearch 多集群（5000+ 节点） / Prometheus / ELK 一体化监控 / 数仓建模与 Hive / Spark SQL
- **阿里云产品**：DataWorks / MaxCompute / EMR Serverless Spark + DLF / Hologres / 实时 Flink / 湖仓迁移、双跑与成本优化
- **工程与语言**：Java / Scala / Python / Shell / Kubernetes / Ansible 自动化 / Redis / MongoDB / MySQL / 150+ Agent Skill / Harness

## 技术栈

- **开源大数据**：Hadoop / Hive / HDFS / YARN / Spark / Flink / Kafka / Flume / Hudi / HBase / Elasticsearch / Kubernetes / Prometheus / ELK
- **阿里云托管**：DataWorks / MaxCompute / EMR Spark / DLF / Paimon / Hologres / StarRocks / OSS

## 工作经历

前 12 年在开源 Hadoop / Spark / Flink / Kafka / ES 上做引擎与平台：唯品会 Hadoop 引擎核心负责人，拼多多 Flink 1.5 / 1.8 核心引擎研发；近 3.5 年在 TapTap 把这套能力迁到阿里云托管产品，做成游戏广告、推荐、ADN 与训练的业务结果。

### 心动科技 · TapTap  ·  大数据开发工程师

2023.05 – 至今
DataWorks  ·  MaxCompute  ·  EMR Spark  ·  DLF  ·  Paimon  ·  Flink  ·  Hologres  ·  Kafka  ·  StarRocks

负责广告 / 推荐 / ADN 核心数据链路的方案设计、实时与离线架构、成本优化与湖仓升级。对内服务业务团队，对外深度使用并反馈阿里云大数据产品。

#### 1. 游戏广告实时特征体系：从 Android 到 iOS，从项目到平台

2024 – 2025  ·  实时特征 / 广告变现 / IEM 特征平台 / Flink

天级特征无法支撑首页广告实时决策，iOS 侧能力缺失，特征开发效率低且难复用到推荐模型。

- **全量实时化**：设计并落地 user / item 及 app、material、UGC 维度非天级特征，完成首页推荐实时数据准确归因。
- **端侧补齐**：将实时特征能力从 Android 扩展到 iOS，补齐关键业务短板，获得业务团队正向反馈。
- **平台沉淀**：主导首页特征实时化重构，方案同步用于广告与推荐两类核心模型，并沉淀至 IEM 特征平台，提升复用与迭代效率。

- 结果：首页广告效果提升 2%+，保守折合年收入增加 2,000 万元以上
- 结果：精细化实时特征工程后核心 CPM 提升约 5%
- 结果：安装特征与 iOS 特征开发效率显著提升，特征结果可复用于推荐模型

#### 2. ADN / 主站实时数据链路重构：用对产品组合同时打成本与时效

2024  ·  Flink / Hologres / 实时数仓 / 成本优化

ADN 日志与串联链路成本高、时效差；主站实时流量分流规则僵化，稳定性问题会放大到后续链路。

- **主站 DWD**：重构分流规则，支持动态分流与配置热加载，修复多类缺陷，实现流量自适应与标准化，降低对下游影响。
- **ADN 日志实时化**：调研数据处理需求并重设计实时方案，在稳定性、查询效率与灵活性上同时提升。
- **串联链路**：采用 Flink + Hologres 重构 ADN 广告串联数据链路，将实时性提升至约 1 分钟。
- **预估日志**：完成广告预估日志实时化开发与保障，支撑多个下游消费方的常态化需求。

- 结果：ADN 请求日志链路月成本降低约 80%（约 4 万元/月）
- 结果：ADN 串联链路月成本降低约 75%（约 4.5 万元/月），投放效果显著提升

#### 3. 下一代湖仓架构：从厂商调研、POC 到 PB 级真实业务双跑

2025 – 2026  ·  Lakehouse / EMR Spark / DLF / 迁移 / POC

公司推进自主可控与 Data + AI 方向，需在保留业务连续性的前提下，评估 MaxCompute 迁出路径，并验证 Spark on 数据湖能否承接广告 / 训练真实负载。

- **选型论证**：与多家云厂商及行业数据中台深度交流，明确以开源架构（Spark on 数据湖）为目标形态；完成 Spark on OSS + DLF 关键路径验证，并对 MC 迁移做成本与风险评估。
- **真实业务 POC → MVP**：针对 ADN iOS 模型训练输出端到端可行性报告，并将 POC 扩大为真实迁移 workflow：schema / 类型对齐、DDL 对比、数据同步、任务元数据迁移、任务翻译、数据验证。
- **Runtime 负责**：主导 DataWorks + EMR Serverless Spark + DLF 运行环境问题排查与多方协同，覆盖权限注入、UDF/函数语义、Paimon scan、snapshot 过期、资源不足、长任务稳定性。
- **迁移服务化**：建设全增量同步、T-3 截断、分区适配、动态表范围、历史缺失分区回补、元数据/schema 一致性、owner 转交、生命周期修复，支撑 900+ 表进入双跑。
- **存储与查询治理**：推进 DLF 存储治理；用 Spark 作业链路与 StarRocks 物化视图将部分 BI 查询从约 75s 优化到 200ms 级。
- **训练场景落地**：协助 IEM 推荐训练团队将样本处理与训练 IO 切到 EMR Spark + DLF，粗排模型「数据处理 + 训练」从 1.5 天降至 0.5 天。
- **产品缺口回流**：围绕权限/资源隔离、联邦查询、Kyuubi / KB Gateway、session 复用、跨语言 UDF 等卡点形成问题清单与方案判断，推动产品能力对齐湖仓落地。

- 结果：存储 3.7PB 优化到 2.8PB，小文件 650 万降至 160 万
- 结果：ADN 迁移进入双跑，风险在双跑中被系统性收敛，为割接与降本对齐奠基
- 结果：新架构在训练与 BI 场景打出可量化的效率优势，形成可复制迁移 SOP

#### 4. 运行时稳定性与关键组件升级

2026  ·  Kafka / Hologres / 流批一体 / EOS

主 Kafka 集群高峰带宽打满；Hologres 老版本面临产品 EOS 及与周边组件的兼容性故障。

- **Kafka**：推动消费组自动创建能力变更，缓解流量高峰期带宽打满。
- **Hologres**：主导 2.2 → 4.x 升级，解决 EOS 风险及因版本不兼容引发的线上故障。
- **流批一体**：持续验证 DW / Spark / Flink / Holo / StarRocks / DLF / 湖仓表之间的端到端链路，补齐监控、告警、容量评估与故障定位 SOP。

- 结果：把单点迁移工具推进为完整运行体系：Runtime、权限边界、存储迁移与数据一致性闭环
- 结果：用周报持续暴露 DW + Spark + DLF 功能缺口与运行风险，形成可复用问题清单

### 哔哩哔哩  ·  资深研发工程师（3-3）

2022.09 – 2022.12
Flink  ·  Kubernetes  ·  Hudi  ·  Kafka

加入实时计算团队，负责 Flink 容器化，以及 Flink + Apache Hudi 湖仓基建的搭建与业务支持。这是开源实时引擎入湖的完整一环，也是后来在 TapTap 做湖仓一体的引擎侧手感。

- **Flink 容器化**：负责实时计算团队 Flink 作业容器化落地，把作业交付、扩缩容从物理集群解耦到 Kubernetes。
- **Flink + Hudi**：参与 Flink 结合 Apache Hudi 的实时入湖链路：作业接入、表格式、compaction / 运维支持，服务业务入湖需求。

### 声网 Agora  ·  架构师 / Leader

2020.08 – 2022.09
Flink  ·  Spark  ·  YARN  ·  Kafka  ·  Prometheus  ·  Elasticsearch  ·  Jenkins

主导开源 Flink 实时计算平台从调研到自研发行版稳定迭代（YARN 部署），并同时负责 Elasticsearch 稳定性、Prometheus 监控一体化和混合云交付。音视频场景对延迟与故障恢复的要求，直接对应后来游戏侧的实时数据底座。

- **自研 Flink 发行版**：设计 Agora 自有 Flink 实时计算平台，简化组件依赖，迭代三个版本；基于 YARN REST API 做作业监控；merge 社区 900+ patch（FLIP-145 TVF / 152 Hive 兼容 / 165 火焰图 / 136 流表互操作 / 162 时间函数），并用 Jenkins 建立社区标准 CI/CD，方便业务提交 patch。
- **引擎能力**：优化维度表 temporal join 与延迟数据即时 join，治理状态泄漏；提供 SQL 脚手架与公共 UDF；Kafka sink 支持 dynamic topic，idle source 水位自增。
- **Spark → Flink 迁移**：将承担上报日志分发的 Spark routing（峰值约 2000 万 QPS）迁到 Flink，涉及作业 100+，压住高峰波动并提升资源利用率。
- **监控一体**：用 Prometheus 收敛原先 Zabbix / InfluxDB / OpenTSDB 多套体系，打通主机 / 组件 / 业务与 owner，监控覆盖提升 90%；告警规则 0 → 120+，指标 10000+。
- **ES 稳定性**：统一集群配置与灰度变更，自动摘盘重启，日志 + JMX + exporter 告警，稳定性从 95% 提升到 99.9%。
- **混合云与成本**：推动国内数据中心方案与混合云初步建设；29 个集群 / 300+ 老网络服务器改造、200+ 过保下线；资源交付周期 60 天 → 1 天，组件交付 7 天 → 4 小时。

- 结果：实时计算从「能跑」做成可迭代的公司级平台，并具备多数据中心互监控与业务切换支撑
- 结果：私有化 / 混合云交付能力成型，为后续安全合规和快速复制打下基础

### 拼多多  ·  架构师 / Flink 核心引擎研发

2018.04 – 2020.07
Flink 1.5 / 1.8  ·  Kubernetes  ·  Kafka  ·  HDFS  ·  Elasticsearch

Flink 核心引擎研发：基于 Flink 1.5 / 1.8 做引擎开发、性能调优、热重启 / 热更新与 checkpoint 治理；同时把 Flink on Kubernetes 做成可量化的计算平台，并负责 100+ Elasticsearch 集群。电商大促下的配额、超卖与跨集群恢复，是后来做云上成本与弹性方案的底子。

- **Flink 核心引擎**：基于 Flink 1.5 / 1.8 做引擎侧研发与源码级调优：热重启 / 热更新缩短作业发布与验证时长；增量 checkpoint 与小文件合并保障长作业稳定；参与 JM/TM 心跳剥离、HDFS 配置统一、启动日志优化等 feature，并支持 connector 开发与作业升级答疑。
- **Flink on K8s**：改造 Heapster，将 K8s 指标流式写入 Kafka，建设 Flink 计算资源大盘；覆盖 10+ 集群、约 15k node、1.5k 作业；灰度发布与跨集群 HA。
- **Quota 与大促**：按部门 / 业务线 / NS / queue 量化分摊，作业 dry run 与最优队列推荐，支撑大促资源评估和碎片利用。
- **ES 多集群**：统一配置与监控，管理集群 100+、节点 5000+、单集群索引 1000+，业务覆盖订单、支付、搜索、广告、推荐、云原生。

- 结果：Flink 作业发布从「停作业再发」做成可热更新 / 热重启，大促期间计算资源可按业务线讲清楚
- 结果：ES 运维从人肉变成平台，作业启动失败风险下降

### 唯品会  ·  Hadoop 引擎核心负责人

2016.04 – 2018.04
Hadoop  ·  MapReduce  ·  Hive  ·  YARN  ·  HDFS  ·  Flume  ·  Kafka  ·  ELK

公司 Hadoop 引擎核心负责人：对 800+ 节点离线计算引擎（MapReduce / Hive / HDFS / YARN）的稳定性、源码调优、版本升级与热升级负责，而不是只做集群运维。同时补齐 Flume / Kafka / ELK 采集链路。

- **Hadoop 引擎**：主导 Hadoop 引擎日常稳定性与源码级调优，patch 开发与迁移，制定灰度变更和热升级方案，800+ 节点处理能力与稳定性提升。
- **YARN 与跨 DC**：优化 YARN 本地性调度，跨数据中心流量下降约 50%；推动业务按数据中心拆分并提供快速迁移。
- **Flume / Kafka / ELK**：负责 Flume、Kafka 分区均衡与迁移工具；基于 ELK 采集 Spark Driver、Storm、HDFS NN 与 audit 日志；Flume 快速索引到 Elasticsearch，支持主键自定义。

- 结果：离线引擎可热升级、可灰度，跨 DC 流量下降约一半，采集与检索链路从散装变成可运维系统

### 五八同城  ·  高级工程师

2015.03 – 2016.04
Hadoop  ·  Hive  ·  HBase  ·  Flume  ·  Kafka  ·  Scala

- **虫洞埋点**：核心开发无痕埋点平台，统一 PC / M / App 三端日志；Flume 落地 Hadoop，Kafka 接入增加 IP 过滤与 token，并用 Scala 做基础 ETL。
- **Hadoop 数据平台**：主导 Hadoop / Kafka 平台运维：集群扩容、资源调度与 Job 分析、HDFS 安全、HBase 对外 API，以及 Flume 日志收集容错与监控告警。

### 郊区电信实业  ·  开发工程师

2010.07 – 2015.03
Hadoop  ·  Hive  ·  Spark  ·  MongoDB

- **电网平台**：参与国家电网工程设计评审平台的功能设计、需求开发与测试。
- **广告统计**：负责广告统计分析平台架构与 MongoDB 设计；业务量上来后迁到 Hadoop / Hive / Spark，做跨月多维统计与实时运营分析，支撑 UV / PV 与精准投放。

## 阿里云大数据 Agent Harness（在研 / 个人工程）

面向 DataWorks 体系的日常开发与运维，覆盖闭源 MaxCompute 与 EMR Serverless Spark + DLF 湖仓链路。以真实线上问题为样本，将排障、开发、运维解法结构化为约 150 条可调用 Skill，而不是散落在聊天记录里。

正在构建面向阿里云大数据平台的 Harness：指令、工具边界、校验与反馈闭环、人工确认。让 Agent 在权限与平台约束内完成查表、排作业、对账、定位失败任务等高频动作，避免对生产作业做不可逆操作。

目标是把「会用平台的人」的经验编码进仓库与工具层，使同类问题可复现、可校验、可交给 Agent 执行，从而降低个人重复劳动，也降低业务使用大数据开发数据应用的复杂度。

## 教育与认证

三峡大学 · 信息与计算科学 · 理学学士 · 2006.09 – 2010.06
