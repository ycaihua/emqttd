
eMQTTD ChangeLog
==================

v0.8.0-alpha (2015-03-20)
-------------------------

MQTT/WebSocket

v0.7.0-alpha (2015-03-20)
-------------------------

Admin Console

v0.6.0-alpha (2015-03-20)
-------------------------

Plugin Architecture

Mnesia Authentication

MySQL Auth

LDAP Auth

PG Auth

Mnesia ACL

MySQL ACL


v0.5.1-alpha (2015-03-13)
-------------------------

Change: upgrade esockd to v1.2.0-beta, rename 'acceptor_pool' to 'acceptors'


v0.5.0-alpha (2015-03-12)
-------------------------

RENAME 'emqtt' to 'emqttd'!

Support [Broker Bridge](https://github.com/emqtt/emqttd/wiki/Bridge-Design) Now!

Change: rename project from 'emqtt' to 'emqttd'

Change: lager:debug to dump RECV/SENT packets

Feature: emqttd_bridg, emqttd_bridge_sup to support broker bridge

Feature: emqtt_event to publish client connected/disconnected message to $SYS topics

Feature: ./bin/emqttd_ctl add more commands: listeners, broker, bridges, start_bridge, stop_bridge...

Feature: issue#57 - support to configure max packet size

Feature: issue#68 - if sys_interval = 0, emqttd_broker will not publish messages to $SYS/brokers/#

Bugfix: issue#67 - subscribe '#' to receive all messages

Bugfix: issue#64 - emqtt_app start/2: should wait_for_databases

Test: emqttd_topic_tests add more '_match_test'


v0.4.0-alpha (2015-03-10)
-------------------------

Support [$SYS Topics of Broker](https://github.com/emqtt/emqttd/wiki/$SYS-Topics-of-Broker) Now!

Feature: emqtt_broker to publish version, uptime, datetime to $SYS/brokers/# topics

Feature: emqtt_broker to publish count of clients, sessions, suscribers to $SYS/brokers/# topics

Feature: emqtt_metrics to publish bytes, packets, messages metrics to $SYS/brokers/# topics

Feature: add include/emqtt_systop.hrl

Change: emqtt_cm to count current clients

Change: emqtt_sm to count current sessions

Change: emqtt_pubsub to count current topics and suscribers

Change: emqtt_pubsub to add create/1 API

Change: emqtt_pubsub dispatch/2 to return number of subscribers

Change: emqtt_pubsub to count 'dropped' messages

Change: emqtt_opts to add merge/2 function

Test: add emqtt_serialiser_tests.erl


v0.3.4-beta (2015-03-08)
------------------------

Bugfix: emqtt_serialiser.erl cannot serialise UNSUBACK packets


v0.3.3-beta (2015-03-07)
------------------------

Bugfix: emqtt_serialiser.erl cannot serialise PINGRESP issue#60


v0.3.2-beta (2015-03-05)
------------------------

Improve: merge emqttc serialiser, parser, packet

Add: emqtt_opts to merge socket options


v0.3.1-beta (2015-03-02)
------------------------

Feature: SSL Socket Support

Feature: issue#44 HTTP API should add Qos parameter

Bugfix: issue#52 emqtt_session crash

Bugfix: issue#53 sslsocket keepalive error

Upgrade: esockd to v0.2.0

Upgrade: mochiweb to v3.0.0


v0.3.0-beta (2015-01-19)
------------------------

Feature: HTTP POST API to support 'qos', 'retain' parameters

Feature: $SYS system topics support

Change: Rewrite emqtt_topic.erl, use '', '#', '+' to replace <<"">>, <<"#">>, <<"+">>

Change: fix emqtt_pubsub.erl to match '#', '+'

Tests: emqtt_topic_tests.erl add more test cases


v0.3.0-alpha (2015-01-18)
------------------------

NOTICE: Full MQTT 3.1.1 support now!

Feature: Passed org.eclipse.paho.mqtt.testing/interoperability tests

Feature: Qos0, Qos1 and Qos2 publish and suscribe

Feature: session(clean_sess=false) management and offline messages

Feature: redeliver awaiting puback/pubrec messages(doc: Chapter 4.4)

Feature: retain messages, add emqtt_server module

Feature: MQTT 3.1.1 null client_id support

Bugfix: keepalive timeout to send will message 

Improve: overlapping subscription support

Improve: add emqtt_packet:dump to dump packets

Test: passed org.eclipse.paho.mqtt.testing/interoperability

Test: simple cluster test

Closed Issues: #22, #24, #27, #28, #29, #30, #31, #32, #33, #34, #36, #37, #38, #39, #41, #42, #43


v0.2.1-beta (2015-01-08)
------------------------

pull request 26: Use binaries for topic paths and fix wildcard topics

emqtt_pubsub.erl: fix wildcard topic match bug caused by binary topic in 0.2.0 

Makefile: deps -> get-deps

rebar.config: fix mochiweb git url

tag emqtt release accoding to [Semantic Versioning](http://semver.org/)

max clientId length is 1024 now.

0.2.0 (2014-12-07)
-------------------

rewrite the project, integrate with esockd, mochiweb

support MQTT 3.1.1

support HTTP to publish message

0.1.5 (2013-01-05)
-------------------

Bugfix: remove QOS_1 match when handle PUBREL request 
 
Bugfix: reverse word in emqtt_topic:words/1 function

0.1.4 (2013-01-04)
-------------------

Bugfix: fix "mosquitto_sub -q 2 ......" bug

Bugfix: fix keep alive bug

0.1.3 (2012-01-04)
-------------------

Feature: support QOS2 PUBREC, PUBREL,PUBCOMP messages

Bugfix: fix emqtt_frame to encode/decoe PUBREC/PUBREL messages


0.1.2 (2012-12-27)
-------------------

Feature: release support like riak

Bugfix: use ?INFO/?ERROR to print log in tcp_listener.erl


0.1.1 (2012-09-24)
-------------------

Feature: use rebar to generate release

Feature: support retained messages

Bugfix: send will msg when network error

0.1.0 (2012-09-21)
-------------------

The first public release.

