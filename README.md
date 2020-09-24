[![License](https://img.shields.io/badge/License-Apache%202.0-green.svg)](https://github.com/funkygao/cp-ddd-framework/blob/master/LICENSE)
[![CI](https://github.com/funkygao/cp-ddd-framework/workflows/CI/badge.svg?branch=master)](https://github.com/funkygao/cp-ddd-framework/actions?query=branch%3Amaster+workflow%3ACI)
[![Code Quality: Java](https://img.shields.io/lgtm/grade/java/g/funkygao/cp-ddd-framework.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/funkygao/cp-ddd-framework/context:java)
[![Total Alerts](https://img.shields.io/lgtm/alerts/g/funkygao/cp-ddd-framework.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/funkygao/cp-ddd-framework/alerts/)
[![Coverage Status](https://img.shields.io/codecov/c/github/funkygao/cp-ddd-framework.svg)](https://codecov.io/gh/funkygao/cp-ddd-framework)
[![TODO](https://badgen.net/https/api.tickgit.com/badgen/github.com/funkygao/cp-ddd-framework?label=todos)](https://www.tickgit.com/browse?repo=github.com/funkygao/cp-ddd-framework)
[![Gitter](https://img.shields.io/gitter/room/cp-ddd-framework/cp-ddd-framework.svg)](https://gitter.im/cp-ddd-framework/community)

# cp-ddd-framework (Central Platform：中台)

* [Building from Source](#building-from-source)
* [What is cp-ddd-framework](#what-is-cp-ddd-framework)
   * [Current status](#current-status)
   * [Quickstart](#quickstart)
   * [What problems does it solve](#what-problems-does-it-solve)
   * [Why it stands out](#why-it-stands-out)
   * [Key abstractions](#key-abstractions)
* [Requirements](#requirements)
* [Demo](#demo)
* [Modules](#modules)
* [Landscape of Central Platform](#landscape-of-central-platform)
* [Reference guide](#reference-guide)
* [Total solutions](#total-solutions)
* [Contribution](#contribution)
* [Licensing](#licensing)

## Building from Source

``` bash
git clone https://github.com/funkygao/cp-ddd-framework.git
cd cp-ddd-framework
mvn clean install
```

## What is cp-ddd-framework?

cp-ddd-framework is a lightweight development framework for complex business architecture.

轻量级业务中台开发框架，以DDD思想为基础，融合业务中台核心要素，赋能业务中台建设。

融合了DDD、前中台复杂生态协作方法论，同时充分考虑组织、历史债、运维和落地成本以及风险而开发的，面向复杂业务场景架构设计，是**业务中台架构的整体解决方案**。

### Current status

目前在多个复杂的中台项目生产环境下使用，保持稳定的前提下积极开发新特性。

**ATTENTION**：Container对Plugin的动态加载，目前仅支持一次性动态加载，热更新机制还在积极开发中，`Container`类已经`@UnderDevelopment`注解，请暂时不要使用。Plugin hotswap mechanism is not production ready yet, please don't use it.

### Quickstart

[快速入门](https://github.com/funkygao/cp-ddd-framework/wiki/Quickstart-%E5%BF%AB%E9%80%9F%E5%85%A5%E9%97%A8)。

Please visit [Quickstart wiki](https://github.com/funkygao/cp-ddd-framework/wiki/Quickstart-%E5%BF%AB%E9%80%9F%E5%85%A5%E9%97%A8).

### What problems does it solve

- born for biz extension, the OCP
- help evolve the system without corruption
- 业务逻辑的个性化：uncertain biz logic
- 业务流程的个性化：uncertain biz flow
- 业务模型的个性化：uncertain biz model
- 业务前台与中台如何协同：synergy between BP and CP teams
- 如何让中台架构特色的DDD稳稳当当落地：DDD seamlessly landing in code
- 如何降低系统实现的复杂度：reduce entropy of the system
- 普通研发如何编写出优雅的业务代码：low threshold for average developer to build elegant biz code
- and more

### Why it stands out

- Simple design and implementation: simplicity is the 1st requirement and less is more
- Flexibility as result of total abstraction
- Totally proven in production environment for complex business requirements

### Key abstractions

这14个核心抽象，勾勒出业务中台的骨架，以不变应万变。

![](http://www.plantuml.com/plantuml/svg/XLHDZziW4BtpApZk7l87h2ZQRTF3IgsqslPUZM4Ses28O9nirVQ_Tt2eOmUgtioynvkFUVWf4WGQ1olYqRWJ11Xa3qvVWY529pkm4HTOx47xYt67xVPYgFz-FUzsaiA8GXX763fGA5_sVW3Zlc8u6uKLWF0a5j-oaVYEQYHyU5onKHcDYH4_lLEfyuPdVuJMOXOiWwmSlBKjgEDQ-aMZ8qC_tZ1wUyPGYdD6TD5ujuHUxNX8scB-ajjVcqrnXnjAd_gUL-ITYOiaNxn6-qm4gX-OdLglnAQXdIndvSxgU61X30n36oc08fbdYUeR3doNy0PzW8ZNBfvROxb4KKHOye0qDyd2DKfdGlmlIMC7ertHYjfMjjZlztp-6Gd8gD-fZe_U4MjYAD7EE9rprS4f5qDt5ak5tGAC5_jYnW2a-eUyyMdkZqAiBRyoHU7s3DOjNAYKUn7tRikAwrvk5gopIyVCDofjJtTUWGY3-pSSo64GbOLl6UOrDDFmryDO8PLYQoDefFKA22lypMRtjyv6jgnPf-HQCsMoI0hFdhfQNIpFiu7IapRkimUDGImeIU3stbEDmD8v4v-LroXoRVbO5fVZvMj8yajBDT87rMDwlSGNnHCwdVxbVm00)

## Requirements

Requires Java 1.8+ and Spring 4.3.12.RELEASE or later.

## Demo

**Tip**: The entry point of the demo is [ExampleTest](cp-ddd-example/order-center-cp/cp-oc-test/src/test/java/org/example/cp/oms/ExampleTest.java).

#### How to run the demo?

``` bash
mvn test -Ptest
mvn install -Pinstall
cd cp-ddd-example/
mvn test -Pdemo
```

你也可以在IDE下手工执行[ExampleTest](cp-ddd-example/order-center-cp/cp-oc-test/src/test/java/org/example/cp/oms/ExampleTest.java)：这是演示的入口。

For more please visit [使用该框架搭建`订单履约中台`的例子](cp-ddd-example).

## Modules

### cp-ddd-spec

Specification of the framework.

### cp-ddd-runtime

Runtime implementation of the framework.

### cp-ddd-enforce

Enforce expected evolvement of the business architecture based upon ArchUnit.

### cp-ddd-test

The complete unit tests.

## Landscape of Central Platform

业务中台建设全景图。

![](doc/assets/img/landscape.png)

## Reference guide

Please go to [cp-ddd-framework Javadoc](https://funkygao.github.io/cp-ddd-framework/doc/apidocs/).

## Total solutions

[业务中台架构的整体解决方案](https://github.com/funkygao/cp-ddd-framework/wiki/Total-solutions-%E6%95%B4%E4%BD%93%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88)。

Please visit [wiki](https://github.com/funkygao/cp-ddd-framework/wiki/Total-solutions-%E6%95%B4%E4%BD%93%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88)

## Contribution

You are welcome to contribute to the project with pull requests on GitHub.

If you find a bug or want to request a feature, please use the [issue tracker](https://github.com/funkygao/cp-ddd-framework/issues).

For any question, you can use [Gitter](https://gitter.im/cp-ddd-framework/community).

## Licensing

cp-ddd-framework is licensed under the Apache License, Version 2.0 (the "License"); you may not use this project except in compliance with the License. You may obtain a copy of the License at [http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0).
