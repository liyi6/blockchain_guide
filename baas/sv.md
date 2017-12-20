## 高性能 BaaS

面向区块链爱好者、开发者的 Devops 平台，托管在某高性能云平台。

区块链管理引擎已开源在 [github.com/yeasy/cello](https://github.com/yeasy/cello)。

### 设计
当初在设计这个平台的时候，目标主要有如下几个：

* 极速响应：申请区块链服务后要秒级提供给用户，主要操作要秒级响应；
* 低成本：物理资源有限，必须低于其它方案 1~2 个数量级的成本；
* 可扩展性：后续添加或减少物理资源的时候，要能方便的进行扩容和缩容；
* 可移植性：要支持多种混合计算架构，以及无论虚机、裸机、公有、私有云；
* 容错性：环境是复杂的，不可靠的，要尽量做到容错，确保系统持续运行；
* 可操作性：带有灵活的管理机制，允许操作人员准确获知系统状态和进行管理。

目前来看，基本达到了当初的设计目标。

### 使用

下面介绍其使用步骤。

访问 [服务首页]()，可以看到正中间的按钮和右上角的登录按钮。

![start](_images/start.jpg)

### 登录和注册

未登录用户，请先点击登录按钮登录。

![](_images/login.jpg)

如果是未注册用户，可以点击登录框内的 `Register` 链接进行注册。

![](_images/register.jpg)

### Dashboard
登录成功后，可以点击申请按钮，如果系统负载没超额度，则申请成功，并自动进入主面板。

![Dashboard](_images/dashboard.jpg)

可以看到，最左面是 `智能合约管理面板`，包括对智能合约的管理和部署，右侧是 `网络面板`，展示申请到的区块链集群的网络情况，包括拓扑、节点之间的延迟信息等一目了然。最下面是 `区块链面板`，是目前区块链的整体情况，初始状态下只有一个区块。

### 智能合约管理
智能合约管理包括部署、使用智能合约，以及上传自己的智能合约。

#### 部署
点击对应智能（如 `map` 合约）合约的 `action` 按钮，会进入合约部署标签页，在这里可以填写合约初始化值，如合约名默认为 `My Chaincode Instance`。

![deploy](_images/deploy.jpg)

点击部署按钮，数秒钟后部署完成，可以在 `My Deployment` 标签页查看到已部署的智能合约。
![mydeploy](_images/mydeploy.jpg)

之后可以通过 `invoke` 按钮调用智能合约。
![invoke](_images/invoke.jpg)

#### 调用合约
调用智能合约，将 `car_owner` 设置为 `Cathy`。

![invoke2](_images/invoke2.jpg)

合约调用后，可以查看区块链情况，生成新的区块。

![blocks](_images/blocks.jpg)

#### 查询合约
合约执行成功后，可以查看合约执行结果，点击 `query` 按钮。

![query](_images/query.jpg)

查询 `car_owner`，可以获取到正确结果。

![query2](_images/query2.jpg)

#### 上传个人合约
个人合约只能自己看到。可以通过点击合约标签页的上传个人合约按钮来完成。
![private_smartcontract](_images/private_smartcontract.jpg)


### 查看区块链日志
在 `网络面板`，点击查看日志按钮，可以打开日志消息记录。

![logs](_images/logs.jpg)

### 重置和退出
用户可以通过点击右上方的用户信息按钮来重置当前区块链或退出。

![operations](_images/user_operations.jpg)
