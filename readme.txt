开发的EA要有的功能:
一、增加交易组（可增加无限交易组，每一组要可设置交易多产品） 二、管理交易组（可修改、删除）
增加每一个交易组要可手动设置项：
1、账户净值x（默认1000）元以下,要交易哪些产品
1.1、要交易的具体产品是x手数起买（默认0.01）
1.2、要交易的具体产品是在x点位开始，是买涨还是买跌（默认正式执行时的点位数，和默认买跌）
1.3、要交易的具体产品止损设几个点
1.4、要交易的具体产品每往买对方向盈利x点，系统要自动增加一个和前单同手数单
1.5、要交易的具体产品每个方向最多增加x个单（默认100）
1.6、要交易的具体产品初始单和增加的单达到设置的止损点数平仓后，系统要立马自动补一个平掉仓的反方向同手数单，累计平仓x单后，后面增加的顺单手数要是前单的x倍
1.7、累积盈利x点数，或x金额后自动结束该产品所有正在执行的单和所有挂单实现锁赢
                                        加一个产品（可加30个以上产品）
设置好每一组后,只要达到设置组的条件，就自动“执行”。
执行后：
1、要自动对先执行组的先交易产品首单按照楼上1.3的设置设置止损，止损点数设置好后，要立刻自动在首单反方向按照楼上1.3的设置点数计算挂第一个、第二个......同手数单(挂单计算公式为：某产品买入/卖入点位减去止损点位数，等于的点位数就是第一个要挂的单买入/卖入点位挂单{例：先执行的某组，先执行的产品是白菜产品，白菜产品设置100点位数买涨，止损设10个点，那反方向第一个挂单应该是90买跌，第二个挂单是80买跌}），挂的每一个单也都需要按照楼上1.3的设置设止损。最多挂单数不要超过楼上1.5设置的单数
2、先执行组的先交易产品首单止损设成功后，及首单反方向要挂的所有单和要挂的所有单止损设成功后。就要自动按照楼上1.4的设置（每往买对方向盈利x点，系统要自动增加一个和前单同手数单）计算挂第一个、第二个......同手数顺单，并为每一个挂的顺单按照楼上的1.3（止损设几个点）设置好止损。最多挂的单数不要超过楼上1.5的设置
3、再后面无论是某产品的初始单，还是后面增加的反单/顺单只要达到楼上1.3设置的止损点数就要自动平仓。平仓后，系统要自动立马按照楼上1.6设置的（初始单和增加的单达到设置的止损点数平仓后，系统要立马自动补一个平掉仓的反方向同手数单，累计平仓x单后，后面增加的顺单手数要是前单的x倍）计算补平掉仓反方向手数挂单，和补仓前面的挂单。
4、再再后面交易组的交易产品达到楼上1.7的设置（盈利x点数，或x金额后自动结束该产品所有正在执行的单和所有挂单实现锁赢）就结束此次该产品的交易，并再自动判断账户有没有超过楼上1（账户净值x（默认1000）元以下）的设置条件，如没超过
，再继续在组结束的交易产品盈利方向自动下一个顺单，并复制上次设置信息启动第二次，第三次...。如果达到楼上1的设置条件，要把该次所有交易的产品正在执行单和挂单全部删除，启动新的一组交易。
注释：任何时间都可手动修改、删除设置的未执行交易组，及可手动删除正在交易的某组某个正在执行单和挂单。

开发的EA要有的功能:
一、增加交易组（可增加无限交易组，每一组可添加多交易产品{至少一个产品}，上可30以上） 二、管理交易组（可新增，修改、删除添加的所有信息）
增加每一个交易组要可手动设置的项：
1、账户净值x（默认1000）元以下,要交易哪些产品，选好每款产品都需要设置以下项：
1.1、x手数起买（默认0.01）
1.2、x点位开始，是买涨还是买跌（默认正式执行时的点位数，和默认买跌）
1.3、该组的该产品执行交易后，以首单买入点位为依据，首单顺方向和首单反方向每隔x点先增加x个反挂单，再增加x个顺挂单（默认100个点）
1.4、首单和新增反、顺挂单止损设x个点
1.5、该组的该产品执行交易后，无论是首单、还是挂单达到设置的止损点数自动平仓后，系统要立马自动补一个平掉仓的反方向同手数单，累计平仓x单后，自动为新补挂单，和原挂的反、顺单增加x倍手数执行买入，和修改
1.6、该组的该产品执行交易后，累积实现盈利x点后，要自动结束该组该产品所有正在执行的单，和所有挂单实现锁赢。
1
设置好每一组保存后,组里面添加的某个产品达到组设置的交易条件，就先自动“执行”交易某个产品。
执行后，按照以下顺序自动处理：
1、楼上1.3的设置
2、楼上1.4的设置
3、楼上1.5的设置
4、楼上1.6的设置
楼上1.6设置实现锁赢后，要再重新自动判断账户有没有超过楼上1的设置条件，如没超过
，再继续在锁赢的产品盈利方向自动下一个顺单，并按照组设置的该交易产品信息，自动执行第二次，第三次...。如果达到楼上1的设置条件，要把该组所有交易的产品正在执行单和挂单全部自动删除，启动新的一组交易。
注释：任何时间都可手动修改、删除设置的未执行交易组，及可手动删除正在交易的某组某个正在执行单和挂单。