# 用multiCall方式获取一个Token持仓用户的余额

#### 需求说明
通过调用合约中的balanceOf()方法，获取一个ERC20 Token持仓用户的余额。
本例中，请获取ETH主链上Uniswap项目UNI Token持仓前10位地址的当前余额。
UNI Token在Etherscan上的地址为：https://etherscan.io/token/0x1f9840a85d5af5bf1d1762f925bdaddc4201f984
其合约地址为：0x1f9840a85d5aF5bf1D1762F925BDADdC4201F984
Holder持仓情况可以在：https://etherscan.io/token/0x1f9840a85d5af5bf1d1762f925bdaddc4201f984#balances 页面看到。
排名前10的持仓地址为：
- 0x1a9c8182c09f50c8318d769245bea52c32be35bc
- 0x4b4e140d1f131fdad6fb59c13af796fd194e4135
- 0x3d30b1ab88d487b0f3061f40de76845bec3f1e94
- 0x47173b170c64d16393a52e6c480b3ad8c302ba1e
- 0xe3953d9d317b834592ab58ab2c7a6ad22b54075d
- 0x0ec9e8aa56e0425b60dee347c8efbad959579d0f
- 0x7d325a9c8f10758188641fe91cfd902499edc782
- 0x090d4613473dee047c3f2706764f49e0821d256e
- 0x090d4613473dee047c3f2706764f49e0821d256e
- 0x7d2d43e63666f45b40316b44212325625dbaeb40

请使用multiCall调用的方式，批量获取这10个市场地址当前时间UNI Token的余额，如排名第一的地址，目前的持仓余额为：`275,436,163.721461187224611866`。

#### 实现要求
- 使用NestJS框架和TypeScript，需要项目能完整运行起来；
- 代码逻辑清晰，NestJS模块划分合理，便于维护和扩展；
- 只请求一次Ethereum节点的RPC即可拿到10个地址的Balance。

#### 参考资料
- [NestJS官方文档](https://docs.nestjs.com/)
- [Ethers.js](https://docs.ethers.io/v5/)
- [Web3.js](https://github.com/ChainSafe/web3.js)
- [MakerDAO Multicall](https://github.com/makerdao/multicall)
- [Multicall.js](https://github.com/makerdao/multicall.js)
