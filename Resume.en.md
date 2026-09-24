[中文](./README.md)

# 洪伟  Wally Hung

16 years in data & realtime architecture  |  X.D. Network · TapTap  ·  Big Data Engineer  ·  May 2023 – Present
177-4081-7241  ·  hongwei200612@gmail.com
China Three Gorges University · Information and Computing Science · B.S. · 2006.09 – 2010.06

## Summary

16 years in big-data and realtime compute. The first 12 years were open-source, self-hosted stacks: Hadoop / Hive / Spark / Flink / Kafka / Elasticsearch / Kubernetes. At Vipshop I owned the Hadoop engine on 800+ nodes (source-level tuning, version and hot upgrades). At Pinduoduo I did Flink 1.5 / 1.8 core engine R&D — performance tuning, hot restart / hot update — and ran Flink on K8s across 15k nodes. At Agora I shipped an in-house Flink distribution (900+ community patches). The last 3.5 years at TapTap I took that same skill set onto Alibaba Cloud DataWorks / MaxCompute / EMR Spark / DLF / Hologres and turned it into business results for gaming ads, recommendation, ADN and training. I can choose, migrate, dual-run and cost-compare between OSS and managed clouds, and encode on-call knowledge into an Agent Harness.

## Selected outcomes

- **+¥20M / yr**: Homepage ad real-time features
- **CPM +5%**: After extending real-time features to iOS
- **TCO −75–80%**: Monthly cost drop on ADN pipelines
- **3.7 → 2.8 PB**: DLF storage governance
- **20M QPS**: Agora Spark routing → Flink migration peak
- **60d → 1d**: Agora hybrid-cloud resource delivery

## Capabilities

- **Open-source compute & storage**: Flink 1.5 / 1.8 engine R&D, tuning, hot restart / Hadoop engine: MR / Hive / HDFS / YARN source-level tuning / Flink on YARN / Kubernetes platforms / Hudi / Paimon lakehouse table formats
- **Realtime ingest & search**: Kafka / Flume / Logstash build & tune / Elasticsearch multi-cluster (5,000+ nodes) / Prometheus / ELK unified observability / Warehouse modeling, Hive / Spark SQL
- **Alibaba Cloud**: DataWorks / MaxCompute / EMR Serverless Spark + DLF / Hologres / realtime Flink / Lakehouse migration, dual-run, TCO
- **Engineering & languages**: Java / Scala / Python / Shell / Kubernetes / Ansible automation / Redis / MongoDB / MySQL / 150+ Agent skills / Harness

## Tech stack

- **Open source**: Hadoop / Hive / HDFS / YARN / Spark / Flink / Kafka / Flume / Hudi / HBase / Elasticsearch / Kubernetes / Prometheus / ELK
- **Alibaba Cloud**: DataWorks / MaxCompute / EMR Spark / DLF / Paimon / Hologres / StarRocks / OSS

## Experience

12 years of engine and platform work on open-source Hadoop / Spark / Flink / Kafka / ES — Hadoop engine owner at Vipshop, Flink 1.5 / 1.8 core engine R&D at Pinduoduo; 3.5 years at TapTap moving that skill set onto Alibaba Cloud managed products for gaming ads, rec, ADN and training.

### X.D. Network · TapTap  ·  Big Data Engineer

May 2023 – Present
DataWorks  ·  MaxCompute  ·  EMR Spark  ·  DLF  ·  Paimon  ·  Flink  ·  Hologres  ·  Kafka  ·  StarRocks

Owned solution design for ads / rec / ADN: realtime and batch architecture, cost, and lakehouse upgrade. Internally served business teams; externally used and stress-tested Alibaba Cloud big-data products.

#### 1. Gaming ads real-time feature platform: Android → iOS, project → platform

2024 – 2025  ·  Real-time features / Ad monetization / IEM / Flink

Day-level features could not support homepage ad decisions; iOS was a gap; feature development was slow and hard to reuse in rec models.

- **Full real-time path**: Designed user/item plus app, material, and UGC non-daily features; delivered accurate homepage attribution.
- **iOS coverage**: Extended the Android capability to iOS, closing a material product gap with positive business feedback.
- **Platformization**: Led homepage feature rebuild; the same design now serves ads and rec models and is landed on the IEM feature platform.

- Result: Homepage ads +2%+ effect, conservatively >¥20M annual revenue
- Result: Core CPM +~5% after finer real-time feature engineering
- Result: Faster install/iOS feature delivery; features reused by rec models

#### 2. ADN / main-site real-time rebuild: the right product mix for TCO and freshness

2024  ·  Flink / Hologres / Realtime DW / TCO

ADN logs and join pipelines were expensive and stale; main-site traffic splitting was rigid and instability amplified downstream.

- **Main-site DWD**: Rebuilt split rules with dynamic routing and hot reload; standardized traffic and cut downstream blast radius.
- **ADN log realtime**: Re-designed the realtime path after a requirements study; stability, query efficiency, and flexibility all improved.
- **Join pipeline**: Rebuilt ADN ad-join on Flink + Hologres; freshness to ~1 minute.
- **Prediction logs**: Shipped realtime prediction-log pipelines for multiple downstream consumers.

- Result: ADN request-log monthly cost −~80% (~¥40k/month)
- Result: ADN join monthly cost −~75% (~¥45k/month), with better delivery performance

#### 3. Next-gen lakehouse: vendor research and POC → PB-scale dual-run

2025 – 2026  ·  Lakehouse / EMR Spark / DLF / Migration / POC

The company needed a controllable Data + AI path off MaxCompute without breaking ads/training, and had to prove Spark-on-lake could carry real load.

- **Architecture choice**: Deep dives with cloud vendors and industry data platforms; target shape Spark-on-lake; validated Spark on OSS + DLF; cost/risk review of MC migration.
- **POC → MVP on real jobs**: End-to-end feasibility for ADN iOS training; expanded into a real migration workflow: schema/types, DDL diff, sync, job metadata, translation, validation.
- **Runtime ownership**: Drove DataWorks + EMR Serverless Spark + DLF environment issues across authz injection, UDF semantics, Paimon scan, snapshot expiry, capacity, long-job stability.
- **Migration as a service**: Full/incremental sync, T-3 truncate, partition adaption, dynamic table scope, backfill, metadata/schema consistency, owner handoff, lifecycle repair — 900+ tables in dual-run.
- **Storage & BI**: DLF storage governance; Spark jobs + StarRocks MVs moved some BI from ~75s to ~200ms.
- **Training cutover**: Helped IEM move sample processing and training IO onto EMR Spark + DLF; coarse-rank data+train 1.5 days → 0.5 day.
- **Product feedback**: Turned authz/resource isolation, federation, Kyuubi/KB Gateway, session reuse, and cross-language UDFs into a reusable gap list for the platform.

- Result: Storage 3.7PB → 2.8PB; small files 6.5M → 1.6M
- Result: ADN migration in dual-run; risks systematically closed ahead of cutover
- Result: Quantified wins on training and BI; reusable migration SOP

#### 4. Runtime stability and component lifecycle

2026  ·  Kafka / Hologres / Stream-batch / EOS

Primary Kafka saturated bandwidth at peaks; Hologres 2.x faced product EOS and compatibility incidents with adjacent components.

- **Kafka**: Changed consumer-group auto-creation to relieve peak bandwidth saturation.
- **Hologres**: Led 2.2 → 4.x upgrade to clear EOS risk and compatibility-driven outages.
- **Unified path**: Kept proving the DW / Spark / Flink / Holo / StarRocks / DLF / lake-table path; filling monitoring, capacity, and incident SOP.

- Result: Moved from one-off migration tools to a runtime system: stability, authz, storage move, and consistency closed-loop
- Result: Weekly exposure of DW + Spark + DLF gaps turned into a reusable issue list

### Bilibili  ·  Senior Engineer (3-3)

Sep 2022 – Dec 2022
Flink  ·  Kubernetes  ·  Hudi  ·  Kafka

Realtime compute team: Flink containerization and Flink + Apache Hudi lakehouse plumbing — the engine-side feel I later used at TapTap.

- **Flink on K8s**: Landed Flink jobs on Kubernetes so delivery and scale-out were less coupled to physical clusters.
- **Flink + Hudi**: Helped stand up Flink + Apache Hudi ingestion: job onboarding, table format, compaction and operational support.

### Agora  ·  Architect / Leader

Aug 2020 – Sep 2022
Flink  ·  Spark  ·  YARN  ·  Kafka  ·  Prometheus  ·  Elasticsearch  ·  Jenkins

Owned the open-source Flink realtime platform from research to a stable in-house distribution on YARN, plus Elasticsearch stability, Prometheus unification and hybrid-cloud delivery. RTC latency and recovery constraints map directly onto later gaming data planes.

- **In-house Flink distro**: Designed Agora’s Flink stack on YARN, three in-house releases, job monitoring via YARN REST API, 900+ community patches (FLIP-145 TVF / 152 Hive compat / 165 flame graph / 136 stream-table / 162 time functions) and Jenkins CI/CD for business-submitted patches.
- **Engine**: Temporal-join freshness, state-leak control, SQL scaffolding and shared UDFs; Kafka sink dynamic topics; idle-source watermark advance.
- **Spark → Flink**: Moved Spark routing that carried report logs (~20M QPS peak) onto Flink, 100+ jobs, cutting peak jitter and raising utilization.
- **Observability**: Collapsed Zabbix/InfluxDB/OpenTSDB into Prometheus; host/component/business/owner mapping; coverage +90%; alert rules 0 → 120+.
- **ES**: Unified config and grey release, auto disk-out restart, log+JMX+exporter alerts; availability 95% → 99.9%.
- **Hybrid cloud**: Domestic DC plan and early hybrid cloud; 29 clusters / 300+ legacy-network hosts / 200+ EOS boxes retired; resource lead time 60d → 1d, component delivery 7d → 4h.

- Result: Realtime compute became a company platform with multi-DC mutual monitoring
- Result: Private/hybrid delivery became a repeatable motion

### Pinduoduo  ·  Architect / Flink core engine R&D

Apr 2018 – Jul 2020
Flink 1.5 / 1.8  ·  Kubernetes  ·  Kafka  ·  HDFS  ·  Elasticsearch

Flink core engine R&D on 1.5 / 1.8: engine features, performance tuning, hot restart / hot update and checkpoint governance. Also turned Flink-on-Kubernetes into a measurable compute platform, and owned 100+ Elasticsearch clusters. Promo-season quota and overcommit are the same conversation as cloud elasticity.

- **Flink engine**: Engine-side work on Flink 1.5 / 1.8: source-level tuning; hot restart / hot update to cut job publish and validation time; incremental checkpoint and small-file compaction for long-running jobs; JM/TM heartbeat split, HDFS config unification, startup-log work; connector support and upgrade Q&A.
- **Flink on K8s**: Streamed Heapster metrics to Kafka and built a Flink compute dashboard across 10+ clusters, ~15k nodes, 1.5k jobs; grey release and cross-cluster HA.
- **Quota**: Chargeback by dept / line / NS / queue, dry-run and best-queue hints for promo planning and fragment packing.
- **ES**: 100+ clusters, 5,000+ nodes, 1,000+ indices per large cluster, spanning order, pay, search, ads, rec and cloud-native teams.

- Result: Flink jobs could hot-update / hot-restart instead of stop-and-ship; compute explainable by business line during promos
- Result: ES ops became a platform; fewer job start failures

### Vipshop  ·  Core owner, Hadoop engine

Apr 2016 – Apr 2018
Hadoop  ·  MapReduce  ·  Hive  ·  YARN  ·  HDFS  ·  Flume  ·  Kafka  ·  ELK

Core owner of the Hadoop engine: stability, source-level tuning, version upgrades and hot upgrades for MapReduce / Hive / HDFS / YARN on 800+ nodes — engine work, not just cluster ops. Also Flume / Kafka / ELK collection.

- **Hadoop engine**: Day-to-day engine stability and source-level tuning, patch development and migration, grey-change process and hot-upgrade plan on 800+ nodes.
- **YARN & cross-DC**: YARN locality cut cross-DC traffic ~50%; split tenants by DC with a fast-move path.
- **Flume / Kafka / ELK**: Flume/Kafka rebalance tools; ELK for Spark driver, Storm, HDFS NN and audit; Flume index-into-Elasticsearch with custom primary keys.

- Result: Offline engine could grey and hot-upgrade; cross-DC traffic roughly halved; ingest and search became operable systems

### 58.com  ·  Senior Engineer

Mar 2015 – Apr 2016
Hadoop  ·  Hive  ·  HBase  ·  Flume  ·  Kafka  ·  Scala

- **Wormhole tracking**: Core dev on a no-trace tracking platform unifying PC/M/App logs; Flume to Hadoop; Kafka ingest with IP filter and token; Scala ETL.
- **Hadoop data platform**: Hadoop / Kafka ops: cluster expansion, resource and job analysis, HDFS security, HBase APIs, Flume collection failover and alerting.

### 郊区电信实业  ·  Software Engineer

Jul 2010 – Mar 2015
Hadoop  ·  Hive  ·  Spark  ·  MongoDB

- **State Grid**: Feature design, delivery and tests for a State Grid engineering-review platform.
- **Ad analytics**: Architecture and MongoDB design for an ad stats platform; later Hadoop / Hive / Spark for cross-month stats and realtime ops, UV/PV and targeting as volume grew.

## Alibaba Cloud big-data Agent Harness (personal / in progress)

Built around daily DataWorks development and ops, covering closed-source MaxCompute and EMR Serverless Spark + DLF. Real incidents are encoded as ~150 callable skills — not lost in chat logs.

The Harness defines instructions, tool boundaries, validation/feedback loops, and human confirmation so an agent can inspect tables, jobs, reconciliation, and failed tasks inside platform permissions — never irreversible production writes.

The point is agent engineering, not a demo: encode “people who know the platform” into the repo so the same work is repeatable, checkable, and delegable.

## Education & certifications

China Three Gorges University · Information and Computing Science · B.S. · 2006.09 – 2010.06
