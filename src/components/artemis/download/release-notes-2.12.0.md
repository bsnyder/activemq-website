---
layout: default_md
title: ActiveMQ Artemis 2.13.0 Release Notes
title-class: page-title-artemis
type: artemis
---

A complete list of JIRAs for the 2.12.0 release can be found [here](https://issues.apache.org/jira/secure/ReleaseNote.jspa?version=12346675&styleName=Text&projectId=12315920&Create=Create&atl_token=A5KQ-2QAV-T4JA-FDED_3276fb93ed0bcc7a73253cccadc445be587a276d_lout)

A list of commits can be found [here](commit-report-2.12.0).

Release Notes - ActiveMQ Artemis - Version 2.12.0




## Bug
    * [ARTEMIS-975] - Reading messages from page causes lost entries in db backend
    * [ARTEMIS-2176] - RA connection properties are not propagated to XARecoveryConfig
    * [ARTEMIS-2325] - SendAcknowledgementHandler when multiple mesages are sent
    * [ARTEMIS-2476] - New MQTT subscriptions receive older (not last published) retained message.
    * [ARTEMIS-2544] - Remove rolledback PageTransactionInfo to free up memory
    * [ARTEMIS-2576] - NullPointerException during AMQP SECURITY_AUTHENTICATION_VIOLATION notification handling
    * [ARTEMIS-2597] - Memory Leak when closing AMQP Consumers in the context
    * [ARTEMIS-2599] - DescribeJournal isn't correctly counting surviving msg
    * [ARTEMIS-2603] - Deadlock on testsuite: PagingStoreImpl::getCurrentIDs is a read operation
    * [ARTEMIS-2606] - Artemis Admin Web Console not loading on server with many queues
    * [ARTEMIS-2607] - Interceptor returns false but processing continues
    * [ARTEMIS-2608] - ClassCastException when consuming a message using OpenWire
    * [ARTEMIS-2612] - artemis-plugin-war manifest
    * [ARTEMIS-2622] - Replication on paging eventually erroring on page already closed.
    * [ARTEMIS-2625] - testListConsumers failing on IBM JDK 8
    * [ARTEMIS-2626] - Postgresql Journal implementation requires the jdbc driver to be in the same classloader
    * [ARTEMIS-2627] - simpleSecureServer failing on IBM Java 8 JVM
    * [ARTEMIS-2629] - Queue never auto-deleted after last message expires
    * [ARTEMIS-2631] - Orphaned address from JMS temp queue
    * [ARTEMIS-2637] - Resilience around UDP Discovery
    * [ARTEMIS-2639] - Lost notification properties when using OpenWire client with a divert 
    * [ARTEMIS-2640] - Audit log messages AMQ601065 and AMQ601072 interpolate the queue name into the user name field
    * [ARTEMIS-2641] - Openwire client runs out of credits after reconnection
    * [ARTEMIS-2642] - Client Drain requests can cause long drain times and client Timeouts
    * [ARTEMIS-2643] - Allow masked password when resetting user via management
    * [ARTEMIS-2645] - Refactor CLI FQQN support
    * [ARTEMIS-2647] - JDBC store query append-to-file not correct for mysql
    * [ARTEMIS-2650] - The delivering count is wrong after reconnecting an openwire client
    * [ARTEMIS-2656] - NPE with read-whole-page == true
    * [ARTEMIS-2658] - AMQP message read from page has wrong encode size
    * [ARTEMIS-2659] - AMQP integration test instabilities, failure to deliver messages, etc
    * [ARTEMIS-2661] - AMQP Journal loading is triggering reencode
    * [ARTEMIS-2662] - Page is broken for AMQP if readWholePage=true
    * [ARTEMIS-2664] - The prefetch size is exceeded after delivered acks
    * [ARTEMIS-2667] - NPE when clearing non-persistent duplicate ID cache
    * [ARTEMIS-2668] - Wrong formatting Strings in class LoggingResultSet
    * [ARTEMIS-2669] - ARTEMIS-2669 not durable AMQP messages cannot became durable on depaging
    * [ARTEMIS-2671] - Hard-coded search in LegacyLDAPSecuritySettingPlugin listener
    * [ARTEMIS-2672] - Multiple threads creating shared subscription can lead to issues.
    * [ARTEMIS-2673] - PageStore should only be removed when Address is removed
    * [ARTEMIS-2681] - Timestamp not set on notification messages
    * [ARTEMIS-2684] - NullPointer exception when slave tries to scale down
    * [ARTEMIS-2685] - Openwire should not block netty thread
    * [ARTEMIS-2686] - Fix MQTT connect message rejection
    * [ARTEMIS-2688] - FileStoreMonitor.calculateUsage Should Check for NaN
    * [ARTEMIS-2702] - QuorumVoteServerConnect with requestToStayLive is voting order sensitive
    * [ARTEMIS-2706] - outgoing AMQP messages split into an unexpectedly large number of transfer frames
    * [ARTEMIS-2708] - JDK bug causes missed properties reload
    * [ARTEMIS-2711] - Use peer host & port for acceptor's SSL engine
    * [ARTEMIS-2712] - updated large message handling not accounted for in aborted message cleanup
    * [ARTEMIS-2713] - Master failback can trigger a useless quorum vote on slave failover
    * [ARTEMIS-2724] - The setting auto-delete-created-queues doesn't work
    * [ARTEMIS-2728] - Deadlock on LargeMessage processing
    * [ARTEMIS-2729] - JdbcLeaseLock won't work on SQL Server



## New Feature
    * [ARTEMIS-1194] - SOCKS proxy support
    * [ARTEMIS-1975] - Real LargeMessage support for AMQP
    * [ARTEMIS-2587] - ActiveMQ5-like dead letter strategy
    * [ARTEMIS-2613] - Support DivertBindings for Federated Addresses
    * [ARTEMIS-2624] - Auto-create expiry resources
    * [ARTEMIS-2692] - Provide Improved API for Queue Creation

## Improvement
    * [ARTEMIS-1676] - Allow users to override JAVA_ARGS via environment variables
    * [ARTEMIS-1953] - Fix Object conversions for AMQP LargeMessages
    * [ARTEMIS-2571] - Remove unneccessary synchronization in ActiveMQServerImpl
    * [ARTEMIS-2602] - Improve Journal loading heap usage
    * [ARTEMIS-2604] - Improve Journal loading heap usage
    * [ARTEMIS-2610] - Improve ActiveMQServer.getConnectionCount()
    * [ARTEMIS-2617] - Improve AMQP Journal loading
    * [ARTEMIS-2619] - Allow "server" header in STOMP CONNECTED frame to be disabled
    * [ARTEMIS-2636] - Expose disk store used percentage metric
    * [ARTEMIS-2644] - Include client id into non durable subscriber queue name
    * [ARTEMIS-2663] - Add customizer support for the embedded web server
    * [ARTEMIS-2674] - AMQP should use a separate executor for IO
    * [ARTEMIS-2676] - PageCursorProviderImpl::cleanup can save decoding pages without large messages
    * [ARTEMIS-2691] - Improve critical analyzer LOG policy
    * [ARTEMIS-2693] - Improve log of starting acceptor errors
    * [ARTEMIS-2695] - Return error message in AMQP response after failed conversion
    * [ARTEMIS-2698] - Expose queue group attributes
    * [ARTEMIS-2699] - Warn if queue stats are limited by default maxRows
    * [ARTEMIS-2701] - Update delivery / DLQ check to be resilient to record not existent
    * [ARTEMIS-2714] - Log details for "Address already in use"
    * [ARTEMIS-2715] - Master broker created with --replicated should use vote-on-replication-failure=true
    * [ARTEMIS-2723] - Read the default CLI connector from the related broker

## Test
    * [ARTEMIS-2725] - Implement a way to retry flaky tests on the testsuite


## Task
    * [ARTEMIS-2598] - Update netty version to 4.1.43.Final
    * [ARTEMIS-2600] - Update mqtt-client version to 1.16
    * [ARTEMIS-2601] - Update jetty version to 9.4.26.v20200117
    * [ARTEMIS-2615] - Update netty version to 4.1.45.Final
    * [ARTEMIS-2646] - Allow setting message properties when sending messages via REST
    * [ARTEMIS-2652] - Fix PageCursorProviderImplTest on IBM JVM
    * [ARTEMIS-2653] - Update to Proton-J 0.33.4 and Qpid JMS 0.50.0
    * [ARTEMIS-2665] - AMQP Shared Non Durable queues are not being created same as CORE
    * [ARTEMIS-2679] - Deprecate message-expiry-thread-priority
    * [ARTEMIS-2703] - Update commons-configuration2 version to 2.7
    * [ARTEMIS-2709] - Fix  LiveToLiveFailoverTest::scaleDownDelay
    * [ARTEMIS-2721] - Activation keeps retrying even after server.stop()
    * [ARTEMIS-2722] - Separate tests for FileLockNodeManager
    * [ARTEMIS-2727] - Update netty version to 4.1.48.Final