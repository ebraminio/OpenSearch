## 2022-05-19 Version 2.0.0 Release Notes

### Breaking Changes in 2.0

#### Remove Mapping types
* [Type removal] Remove redundant _type in pipeline simulate action  ([#3371](https://github.com/opensearch-project/OpenSearch/pull/3371))
* [Type removal] Remove _type deprecation from script and conditional processor  ([#3239](https://github.com/opensearch-project/OpenSearch/pull/3239))
* [Type removal] Remove _type from _bulk yaml test, scripts, unused constants  ([#3372](https://github.com/opensearch-project/OpenSearch/pull/3372))
* [Type removal] _type removal from mocked responses of scroll hit tests  ([#3377](https://github.com/opensearch-project/OpenSearch/pull/3377))
* [Remove] TypeFieldMapper  ([#3196](https://github.com/opensearch-project/OpenSearch/pull/3196))
* [Type Removal] Remove TypeFieldMapper usage, remove support of `_type` in searches and from LeafFieldsLookup  ([#3016](https://github.com/opensearch-project/OpenSearch/pull/3016))
* [Type removal] Remove _type support in NOOP bulk indexing from client benchmark ([#3076](https://github.com/opensearch-project/OpenSearch/pull/3076))
* [Type removal] Remove deprecation warning on use of _type in doc scripts ([#2564](https://github.com/opensearch-project/OpenSearch/pull/2564))
* [Remove] AliasesExistAction ([#3149](https://github.com/opensearch-project/OpenSearch/pull/3149))
* [Remove] TypesExist Action ([#3139](https://github.com/opensearch-project/OpenSearch/pull/3139))
* [Remove] Type from nested fields using new metadata field mapper([#3004](https://github.com/opensearch-project/OpenSearch/pull/3004))
* [Remove] types from rest-api-spec endpoints ([#2689](https://github.com/opensearch-project/OpenSearch/pull/2689))
* [Remove] Types from PutIndexTemplateRequest and builder to reduce mapping to a string ([#2510](https://github.com/opensearch-project/OpenSearch/pull/2510))
* [Remove] Type from Percolate query API ([#2490](https://github.com/opensearch-project/OpenSearch/pull/2490))
* [Remove] types from CreateIndexRequest and companion Builder's mapping method ([#2498](https://github.com/opensearch-project/OpenSearch/pull/2498))
* [Remove] Type from PutIndexTemplateRequest and PITRB ([#2497](https://github.com/opensearch-project/OpenSearch/pull/2497))
* [Remove] Type metadata from ingest documents ([#2491](https://github.com/opensearch-project/OpenSearch/pull/2491))
* [Remove] type from CIR.mapping and CIRB.mapping ([#2478](https://github.com/opensearch-project/OpenSearch/pull/2478))
* [Remove] types based addMapping method from CreateIndexRequest and Builder ([#2460](https://github.com/opensearch-project/OpenSearch/pull/2460))
* [Remove] type from TaskResults index and IndexMetadata.getMappings ([#2469](https://github.com/opensearch-project/OpenSearch/pull/2469))
* [Remove] Type query ([#2448](https://github.com/opensearch-project/OpenSearch/pull/2448))
* [Remove] Type from TermsLookUp ([#2459](https://github.com/opensearch-project/OpenSearch/pull/2459))
* [Remove] types from Uid and remaining types/Uid from translog ([#2450](https://github.com/opensearch-project/OpenSearch/pull/2450))
* [Remove] types from translog ([#2439](https://github.com/opensearch-project/OpenSearch/pull/2439))
* [Remove] Type mapping end-points from RestMultiSearchTemplateAction ([#2433](https://github.com/opensearch-project/OpenSearch/pull/2433))
* [Remove] Multiple Types from IndexTemplateMetadata ([#2400](https://github.com/opensearch-project/OpenSearch/pull/2400))

#### Upgrades
* [Upgrade] Lucene 9.1 release ([#2560](https://github.com/opensearch-project/OpenSearch/pull/2560))
* [Upgrade] ICU4j from 68.2 to 70.1 ([#2504](https://github.com/opensearch-project/OpenSearch/pull/2504))

#### Deprecations
* Deprecate setting 'cluster.no_master_block' and introduce the alternative setting 'cluster.no_cluster_manager_block' ([#2453](https://github.com/opensearch-project/OpenSearch/pull/2453))
* Deprecate setting 'cluster.service.slow_master_task_logging_threshold' and introduce the alternative setting 'cluster.service.slow_cluster_manager_task_logging_threshold' ([#2451](https://github.com/opensearch-project/OpenSearch/pull/2451))
* Deprecate setting 'cluster.initial_master_nodes' and introduce the alternative setting 'cluster.initial_cluster_manager_nodes' ([#2463](https://github.com/opensearch-project/OpenSearch/pull/2463))
* Deprecated reserved node id '_must_join_elected_master_' that used by DetachClusterCommand and replace with '_must_join_elected_cluster_manager_' ([#3138](https://github.com/opensearch-project/OpenSearch/pull/3138))

### Security Fixes
* [CVE-2020-36518] Update jackson-databind to 2.13.2.2 ([#2599](https://github.com/opensearch-project/OpenSearch/pull/2599))

### Features/Enhancements
* Removing hard coded value of max concurrent shard requests ([#3364](https://github.com/opensearch-project/OpenSearch/pull/3364))
* Update generated ANTLR lexer/parser to match runtime version ([#3297](https://github.com/opensearch-project/OpenSearch/pull/3297))
* Rename BecomeMasterTask to BecomeClusterManagerTask in JoinTaskExecutor  ([#3099](https://github.com/opensearch-project/OpenSearch/pull/3099))
* Replace 'master' terminology with 'cluster manager' in log messages in 'server/src/main' directory - Part 2 ([#3174](https://github.com/opensearch-project/OpenSearch/pull/3174))
* Remove deprecation warning of using REST API request parameter 'master_timeout' ([#2920](https://github.com/opensearch-project/OpenSearch/pull/2920))
* Add deprecated API for creating History Ops Snapshot from translog ([#2886](https://github.com/opensearch-project/OpenSearch/pull/2886))
* Add request parameter 'cluster_manager_timeout' and deprecate 'master_timeout' - in Ingest APIs and Script APIs ([#2682](https://github.com/opensearch-project/OpenSearch/pull/2682))
* Change deprecation message for API parameter value 'master_node' of parameter 'metric' ([#2880](https://github.com/opensearch-project/OpenSearch/pull/2880))
* Add request parameter 'cluster_manager_timeout' and deprecate 'master_timeout' - in Snapshot APIs ([#2680](https://github.com/opensearch-project/OpenSearch/pull/2680))
* Add request parameter 'cluster_manager_timeout' and deprecate 'master_timeout' - in Index Template APIs ([#2678](https://github.com/opensearch-project/OpenSearch/pull/2678))
* Change deprecation message for REST API parameter 'master_timeout' to specify the version of removal  ([#2863](https://github.com/opensearch-project/OpenSearch/pull/2863))
* Decouple IndexSettings from IncludeExclude ([#2860](https://github.com/opensearch-project/OpenSearch/pull/2860))
* Remove endpoint_suffix dependency on account key ([#2485](https://github.com/opensearch-project/OpenSearch/pull/2485))
* Replace remaining 'blacklist' with 'denylist' in internal class and method names ([#2784](https://github.com/opensearch-project/OpenSearch/pull/2784))
* Make discovered_master field optional on the client to support compatibility for opensearch client with odfe ([#2641](https://github.com/opensearch-project/OpenSearch/pull/2641))
* Add request parameter 'cluster_manager_timeout' and deprecate 'master_timeout' - in Index APIs except index template APIs  ([#2660](https://github.com/opensearch-project/OpenSearch/pull/2660))
* Add request parameter 'cluster_manager_timeout' and deprecate 'master_timeout' - in Cluster APIs ([#2658](https://github.com/opensearch-project/OpenSearch/pull/2658))
* Make Rest-High-Rest-Level tests allow deprecation warning temporarily, during deprecation of request parameter 'master_timeout' ([#2702](https://github.com/opensearch-project/OpenSearch/pull/2702))
* Add request parameter 'cluster_manager_timeout' as the alternative for 'master_timeout', and deprecate 'master_timeout' - in CAT APIs ([#2717](https://github.com/opensearch-project/OpenSearch/pull/2717))
* Add mapping method back referenced in other repos ([#2636](https://github.com/opensearch-project/OpenSearch/pull/2636))
* Replaced "master" terminology in Log message ([#2575](https://github.com/opensearch-project/OpenSearch/pull/2575))
* Introduce QueryPhaseSearcher extension point (SearchPlugin) ([#1931](https://github.com/opensearch-project/OpenSearch/pull/1931))
* Support for geo_bounding_box queries on geo_shape fields ([#2506](https://github.com/opensearch-project/OpenSearch/pull/2506))
* Updating repository commons logging version ([#2541](https://github.com/opensearch-project/OpenSearch/pull/2541))
* Support for geo_distance queries on geo_shape fields ([#2516](https://github.com/opensearch-project/OpenSearch/pull/2516))
* Add 'cluster_manager_node' into ClusterState Metric as an alternative to 'master_node' ([#2415](https://github.com/opensearch-project/OpenSearch/pull/2415))
* Add a new node role 'cluster_manager' as the alternative for 'master' role and deprecate 'master' role ([#2424](https://github.com/opensearch-project/OpenSearch/pull/2424))
* Replace 'master' with 'cluster_manager' in 'GET Cat Nodes' API ([#2441](https://github.com/opensearch-project/OpenSearch/pull/2441))
* Replace 'discovered_master' with 'discovered_cluster_manager' in 'GET Cat Health' API ([#2438](https://github.com/opensearch-project/OpenSearch/pull/2438))
* Add a field discovered_cluster_manager in get cluster health api ([#2437](https://github.com/opensearch-project/OpenSearch/pull/2437))
* Add request parameter 'cluster_manager_timeout' as the alternative for 'master_timeout', and deprecate 'master_timeout' - in CAT Nodes API ([#2435](https://github.com/opensearch-project/OpenSearch/pull/2435))
* Add a new REST API endpoint 'GET _cat/cluster_manager' as the replacement of 'GET _cat/master' ([#2404](https://github.com/opensearch-project/OpenSearch/pull/2404))
* Add default for EnginePlugin.getEngineFactory ([#2419](https://github.com/opensearch-project/OpenSearch/pull/2419))

### Bug Fixes
* Fixing PublishTests tests (running against unclean build folders) ([#3253](https://github.com/opensearch-project/OpenSearch/pull/3253))
* Fixing Scaled float field mapper to respect ignoreMalformed setting ([#2918](https://github.com/opensearch-project/OpenSearch/pull/2918))
* Fixing plugin installation URL to consume build qualifier ([#3193](https://github.com/opensearch-project/OpenSearch/pull/3193))
* Fix minimum index compatibility error message  ([#3159](https://github.com/opensearch-project/OpenSearch/pull/3159))
* Added explicit 'null' check for response listener to prevent obscure NullPointerException issues  ([#3048](https://github.com/opensearch-project/OpenSearch/pull/3048))
* Adding a null pointer check to fix index_prefix query ([#2879](https://github.com/opensearch-project/OpenSearch/pull/2879))
* Bugfix to guard against stack overflow errors caused by very large reg-ex input ([#2816](https://github.com/opensearch-project/OpenSearch/pull/2816))
* Fix InboundDecoder version compat check  ([#2570](https://github.com/opensearch-project/OpenSearch/pull/2570))
* ignore_malformed parameter on ip_range data_type throws mapper_parsing_exception ([#2429](https://github.com/opensearch-project/OpenSearch/pull/2429))
* Discrepancy in result from _validate/query API and actual query validity ([#2416](https://github.com/opensearch-project/OpenSearch/pull/2416))

### Build & Infrastructure
* Allow to configure POM for ZIP publication  ([#3252](https://github.com/opensearch-project/OpenSearch/pull/3252))
* Gradle plugin `opensearch.pluginzip` Add implicit dependency. ([#3189](https://github.com/opensearch-project/OpenSearch/pull/3189))
* Gradle custom java zippublish plugin ([#2988](https://github.com/opensearch-project/OpenSearch/pull/2988))
* Added Adoptium JDK8 support and updated DistroTestPlugin JDK version used by Gradle  ([#3324](https://github.com/opensearch-project/OpenSearch/pull/3324))
* Update bundled JDK to 17.0.3+7  ([#3093](https://github.com/opensearch-project/OpenSearch/pull/3093))
* Use G1GC on JDK11+ ([#2964](https://github.com/opensearch-project/OpenSearch/pull/2964))
* Removed java11 source folders since JDK-11 is the baseline now ([#2898](https://github.com/opensearch-project/OpenSearch/pull/2898))
* Changed JAVA_HOME to jdk-17  ([#2656](https://github.com/opensearch-project/OpenSearch/pull/2656))
* Fix build-tools/reaper source/target compatibility to be JDK-11  ([#2596](https://github.com/opensearch-project/OpenSearch/pull/2596))
* Adding workflow to create documentation related issues in documentation-website repo ([#2929](https://github.com/opensearch-project/OpenSearch/pull/2929))
* Fix issue that deprecated setting 'cluster.initial_master_nodes' is not identified in node bootstrap check  ([#2779](https://github.com/opensearch-project/OpenSearch/pull/2779))
* Replace blacklist in Gradle build environment configuration ([#2752](https://github.com/opensearch-project/OpenSearch/pull/2752))
* Update ThirdPartyAuditTask to check for and list pointless exclusions. ([#2760](https://github.com/opensearch-project/OpenSearch/pull/2760))
* Add Shadow jar publication to lang-painless module.  ([#2681](https://github.com/opensearch-project/OpenSearch/pull/2681))
* Add 1.3.2 to main causing gradle check failures  ([#2679](https://github.com/opensearch-project/OpenSearch/pull/2679))
* Added jenkinsfile to run gradle check in OpenSearch  ([#2166](https://github.com/opensearch-project/OpenSearch/pull/2166))
* Gradle check retry  ([#2638](https://github.com/opensearch-project/OpenSearch/pull/2638))
* Override Default Distribution Download Url with Custom Distribution Url when it is passed from Plugin ([#2420](https://github.com/opensearch-project/OpenSearch/pull/2420))

### Documentation
* [Javadocs] add remaining internal classes and reenable missingJavadoc on server ([#3296](https://github.com/opensearch-project/OpenSearch/pull/3296))
* [Javadocs] add to o.o.cluster  ([#3170](https://github.com/opensearch-project/OpenSearch/pull/3170))
* [Javadocs] add to o.o.bootstrap, cli, and client  ([#3163](https://github.com/opensearch-project/OpenSearch/pull/3163))
* [Javadocs] add to o.o.search.rescore,searchafter,slice, sort, and suggest ([#3264](https://github.com/opensearch-project/OpenSearch/pull/3264))
* [Javadocs] add to o.o.transport ([#3220](https://github.com/opensearch-project/OpenSearch/pull/3220))
* [Javadocs] add to o.o.action, index, and transport ([#3277](https://github.com/opensearch-project/OpenSearch/pull/3277))
* [Javadocs] add to internal classes in o.o.http, indices, and search ([#3288](https://github.com/opensearch-project/OpenSearch/pull/3288))
* [Javadocs] Add to remaining o.o.action classes ([#3182](https://github.com/opensearch-project/OpenSearch/pull/3182))
* [Javadocs] add to o.o.rest, snapshots, and tasks packages ([#3219](https://github.com/opensearch-project/OpenSearch/pull/3219))
* [Javadocs] add to o.o.common ([#3289](https://github.com/opensearch-project/OpenSearch/pull/3289))
* [Javadocs] add to o.o.dfs,fetch,internal,lookup,profile, and query packages ([#3261](https://github.com/opensearch-project/OpenSearch/pull/3261))
* [Javadocs] add to o.o.search.aggs, builder, and collapse packages ([#3254](https://github.com/opensearch-project/OpenSearch/pull/3254))
* [Javadocs] add to o.o.index and indices  ([#3209](https://github.com/opensearch-project/OpenSearch/pull/3209))
* [Javadocs] add to o.o.monitor,persistance,plugins,repo,script,threadpool,usage,watcher ([#3186](https://github.com/opensearch-project/OpenSearch/pull/3186))
* [Javadocs] Add to o.o.disovery, env, gateway, http, ingest, lucene and node pkgs  ([#3185](https://github.com/opensearch-project/OpenSearch/pull/3185))
* [Javadocs] add to o.o.action.admin ([#3155](https://github.com/opensearch-project/OpenSearch/pull/3155))
* [Javadocs] Add missing package-info.java files to server ([#3128](https://github.com/opensearch-project/OpenSearch/pull/3128))

### Maintenance
* Bump re2j from 1.1 to 1.6 in /plugins/repository-hdfs ([#3337](https://github.com/opensearch-project/OpenSearch/pull/3337))
* Bump google-oauth-client from 1.33.1 to 1.33.2 in /plugins/discovery-gce ([#2828](https://github.com/opensearch-project/OpenSearch/pull/2828))
* Bump protobuf-java-util from 3.19.3 to 3.20.0 in /plugins/repository-gcs ([#2834](https://github.com/opensearch-project/OpenSearch/pull/2834))
* Bump cdi-api from 1.2 to 2.0 in /qa/wildfly ([#2835](https://github.com/opensearch-project/OpenSearch/pull/2835))
* Bump azure-core from 1.26.0 to 1.27.0 in /plugins/repository-azure ([#2837](https://github.com/opensearch-project/OpenSearch/pull/2837))
* Bump asm-analysis from 9.2 to 9.3 in /test/logger-usage  ([#2829](https://github.com/opensearch-project/OpenSearch/pull/2829))
* Bump protobuf-java from 3.19.3 to 3.20.0 in /plugins/repository-hdfs  ([#2836](https://github.com/opensearch-project/OpenSearch/pull/2836))
* Bump joni from 2.1.41 to 2.1.43 in /libs/grok ([#2832](https://github.com/opensearch-project/OpenSearch/pull/2832))
* Bump geoip2 from 2.16.1 to 3.0.1 in /modules/ingest-geoip  ([#2646](https://github.com/opensearch-project/OpenSearch/pull/2646))
* Bump jettison from 1.1 to 1.4.1 in /plugins/discovery-azure-classic ([#2614](https://github.com/opensearch-project/OpenSearch/pull/2614))
* Bump google-oauth-client from 1.31.0 to 1.33.1 in /plugins/repository-gcs  ([#2616](https://github.com/opensearch-project/OpenSearch/pull/2616))
* Bump jboss-annotations-api_1.2_spec in /qa/wildfly  ([#2615](https://github.com/opensearch-project/OpenSearch/pull/2615))
* Bump forbiddenapis in /buildSrc/src/testKit/thirdPartyAudit  ([#2611](https://github.com/opensearch-project/OpenSearch/pull/2611))
* Bump json-schema-validator from 1.0.67 to 1.0.68 in /buildSrc ([#2610](https://github.com/opensearch-project/OpenSearch/pull/2610))
* Bump htrace-core4 from 4.1.0-incubating to 4.2.0-incubating in /plugins/repository-hdfs  ([#2618](https://github.com/opensearch-project/OpenSearch/pull/2618))
* Bump asm-tree from 7.2 to 9.2 in /modules/lang-painless  ([#2617](https://github.com/opensearch-project/OpenSearch/pull/2617))
* Bump antlr4 from 4.5.3 to 4.9.3 in /modules/lang-painless ([#2537](https://github.com/opensearch-project/OpenSearch/pull/2537))
* Bump commons-lang3 from 3.7 to 3.12.0 in /plugins/repository-hdfs ([#2552](https://github.com/opensearch-project/OpenSearch/pull/2552))
* Bump gson from 2.8.9 to 2.9.0 in /plugins/repository-gcs ([#2550](https://github.com/opensearch-project/OpenSearch/pull/2550))
* Bump google-oauth-client from 1.31.0 to 1.33.1 in /plugins/discovery-gce ([#2524](https://github.com/opensearch-project/OpenSearch/pull/2524))
* Bump google-cloud-core from 1.93.3 to 2.5.10 in /plugins/repository-gcs ([#2536](https://github.com/opensearch-project/OpenSearch/pull/2536))
* Bump wiremock-jre8-standalone from 2.23.2 to 2.32.0 in /buildSrc ([#2525](https://github.com/opensearch-project/OpenSearch/pull/2525))
* Bump com.gradle.enterprise from 3.8.1 to 3.9 ([#2523](https://github.com/opensearch-project/OpenSearch/pull/2523))
* Bump commons-io from 2.7 to 2.11.0 in /plugins/discovery-azure-classic ([#2527](https://github.com/opensearch-project/OpenSearch/pull/2527))
* Bump asm-analysis from 7.1 to 9.2 in /test/logger-usage ([#2273](https://github.com/opensearch-project/OpenSearch/pull/2273))
* Bump asm-commons from 7.2 to 9.2 in /modules/lang-painless ([#2234](https://github.com/opensearch-project/OpenSearch/pull/2234))
* Bump jna from 5.5.0 to 5.10.0 in /buildSrc ([#2512](https://github.com/opensearch-project/OpenSearch/pull/2512))
* Bump jsr305 from 1.3.9 to 3.0.2 in /plugins/discovery-gce ([#2137](https://github.com/opensearch-project/OpenSearch/pull/2137))
* Bump json-schema-validator from 1.0.36 to 1.0.67 in /buildSrc ([#2454](https://github.com/opensearch-project/OpenSearch/pull/2454))
* Bump woodstox-core from 6.1.1 to 6.2.8 in /plugins/repository-azure ([#2456](https://github.com/opensearch-project/OpenSearch/pull/2456))
* Bump commons-lang3 from 3.4 to 3.12.0 in /plugins/repository-azure ([#2455](https://github.com/opensearch-project/OpenSearch/pull/2455))
* Update azure-storage-blob to 12.15.0 ([#2774](https://github.com/opensearch-project/OpenSearch/pull/2774))
* Move Jackson-databind to 2.13.2 ([#2548](https://github.com/opensearch-project/OpenSearch/pull/2548))
* Add trademark notice ([#2473](https://github.com/opensearch-project/OpenSearch/pull/2473))
* adds ToC ([#2546](https://github.com/opensearch-project/OpenSearch/pull/2546))
* Sync maintainers with actual permissions. ([#3127](https://github.com/opensearch-project/OpenSearch/pull/3127))

### Refactoring
* [Remove] remaining AllFieldMapper references ([#3007](https://github.com/opensearch-project/OpenSearch/pull/3007))
* Clear up some confusing code in IndexShardHotSpotTests ([#1534](https://github.com/opensearch-project/OpenSearch/pull/1534))
* [Remove] ShrinkAction, ShardUpgradeRequest, UpgradeSettingsRequestBuilder ([#3169](https://github.com/opensearch-project/OpenSearch/pull/3169))
* [Rename] ESTestCase stragglers to OpenSearchTestCase ([#3053](https://github.com/opensearch-project/OpenSearch/pull/3053))
* [Remove] MainResponse version override cluster setting ([#3031](https://github.com/opensearch-project/OpenSearch/pull/3031))
* [Version] Don't spoof major for 3.0+ clusters ([#2722](https://github.com/opensearch-project/OpenSearch/pull/2722))
* Centralize codes related to 'master_timeout' deprecation for eaiser removal - in CAT Nodes API ([#2670](https://github.com/opensearch-project/OpenSearch/pull/2670))
* Rename reference to project OpenSearch was forked from ([#2483](https://github.com/opensearch-project/OpenSearch/pull/2483))
* Remove the IndexCommitRef class ([#2421](https://github.com/opensearch-project/OpenSearch/pull/2421))
* Refactoring gated and ref-counted interfaces and their implementations ([#2396](https://github.com/opensearch-project/OpenSearch/pull/2396))
* [Refactor] LuceneChangesSnapshot to use accurate ops history ([#2452](https://github.com/opensearch-project/OpenSearch/pull/2452))

### Tests
* Add type mapping removal bwc tests for indexing, searching, snapshots ([#2901](https://github.com/opensearch-project/OpenSearch/pull/2901))
* Removing SLM check in tests for OpenSearch versions ([#2604](https://github.com/opensearch-project/OpenSearch/pull/2604))
* [Unmute] NumberFieldTypeTests ([#2531](https://github.com/opensearch-project/OpenSearch/pull/2531))
* Use Hamcrest matchers and assertThat() in ReindexRenamedSettingTests ([#2503](https://github.com/opensearch-project/OpenSearch/pull/2503))
* [Unmute] IndexPrimaryRelocationIT ([#2488](https://github.com/opensearch-project/OpenSearch/pull/2488))
* Fixing PluginsServiceTests (post Lucene 9 update) ([#2484](https://github.com/opensearch-project/OpenSearch/pull/2484))