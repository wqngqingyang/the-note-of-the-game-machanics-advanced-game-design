***
# [《游戏机制：高级游戏设计技术》](https://m.aliyun.com/yunqi/articles/92097?spm=5176.11156381.0.0.7a5d306cHYmX1M)读书笔记 #
***
## 第一章 设计游戏机制 ##
### - 知识导图 ###



<table>
    <tr>
<th rowspan="2">游戏性质 </th>
<td>基于规则</td>   <td>状态机</td>   
      </tr>  <tr>
<td>  不可预测  </td><td>偶然性</td> <td>玩家选择</td><td>复杂规则</td>
      </tr><tr>


<th rowspan="5">游戏机制 </td>
<td rowspan="5">离散机制和连续机制 </td>
<td>物理</td>      <td>♔  </td> <td>    </td><td>    </td><td> ♔    </td><td> ♔    </td><td>    </td><td>    </td><td>  ♔   </td><td>    </td>
      </tr>  <tr>
<td>内部经济</td>   <td> ♪   </td>    <td> ♔    </td><td>♔     </td><td>    </td><td>    </td><td>   ♔  </td><td>    </td><td>    </td><td>   ♔  </td>
      </tr><tr>
<td> 渐进机制   </td><td>  ♪  </td><td>    </td><td>  ♔   </td><td>    </td><td>    </td><td>    </td><td>  ♔   </td><td>    </td><td>    </td>
      </tr><tr>
<td> 战术动机   </td><td>    </td><td>   ♔  </td><td>    </td><td>    </td><td>    </td><td> ♪   </td><td>    </td><td>    </td><td>    </td>
      </tr><tr>
<td> 社交互动   </td><td>    </td><td>  ♪  </td><td>  ♪  </td><td>    </td><td>    </td><td>    </td><td>    </td><td>    </td><td>  ♔   </td>
      </tr><tr>


<td>游戏类型</td>      <td>    </td><td>    </td>  <td>动作</td> <td>策略</td> <td>角色扮演</td> <td>体育</td> <td>驾驶模拟</td> <td>经营模拟</td> <td>冒险</td> <td>益智解谜</td> <td>社交游戏</td>
      </tr>  <tr>


<th rowspan="3">游戏设计流程 </th>
<td>概念设计阶段</td>      <td>   游戏概念 </td>  <td> 目标受众   </td> <td> 核心机制   </td><td> 预期美术风格   </td>
      </tr>  <tr>
<td>详细设计阶段</td>   <td>  创建游戏关卡  </td>   <td>  撰写故事情节  </td> <td>  制作美术资源  </td><td>  等  </td>
      </tr><tr>
<td> 调整阶段  </td><td>   特性冻结</td><td> 减法过程 </td>
      </tr><tr>


<th rowspan="15">原型制作技术 </th>

<th rowspan="2">术语 </th>     <td>   高保真 </td>  <td>  低保真  </td> 
      </tr>  <tr>
<td>水平分片</td>   <td> 垂直分片  </td>  
      </tr><tr>

<th rowspan="3">原型 </th>     <td> 软件原型   </td>  <td>很好地评估可玩性    </td>  <td>耗时长
      </tr>  <tr>

<td> 纸面原型  </td><td>   ①快速②天生易于修改</td><td> ①难上手②适用性弱</td>
      </tr><tr>


<td> 物理原型  </td><td>   准备工作最少</td><td> 难度大 </td>
      </tr><tr>


<th rowspan="1">原型聚焦点 </th>
<td>技术演示</td>      <td>游戏经济</td>     <td>界面和操作方法  </td><td>教程 </td>




   </tr>
   </table>

- 有关资料

[在短时间内开发游戏的7个小提示](www.youtube.com/watch?v=aW6vgW8wc6c)

[Spore](http://www.spore.com/comm/prototypes)的开发原型（并没有时间玩qwq）

实况角色扮演游戏[LAPR](https://www.meetup.com/topics/larp/)

## 第二章 突现和渐进 ##
 

### - 知识导图 ###
<table>
    <tr>

<th rowspan="1"> </th><td>规则数量</td> <td> 游戏要素数量   </td> <td>  各要素交互  </td><td>  概率空间  </td><td> 重玩价值   </td><td> 设计师对流程控制力   </td><td> 游戏长度   </td><td>   学习曲线 </td>

 <tr>

<th rowspan="1">突现型游戏 </th><td> 少   </td><td>   多 </td><td>  多  </td><td>  大而广  </td><td>  高  </td><td> 低   </td><td> 通常较短  </td><td>  通常较陡  </td> <td> 桌上游戏都是    </td>
      </tr>  <tr>




<th rowspan="1">渐近型游戏 </th>
<td> 多   </td><td> 少-多   </td><td>  少 </td><td> 小而深    </td><td>  低  </td><td> 高   </td><td>  通常较长  </td><td> 通常较平缓   </td>  <td> 大量数据或资料，提供设计好的挑战。   </td>
      </tr>  <tr>




</tr>
   </table>


> **突现和渐进一般在游戏中是相结合的**




## 第三章 复杂系统和突现结构 ##


<table>
 
<th rowspan="3">复杂系统 </th>

<td rowspan="3">由单元组成 </td><td> 动态行为
<tr><td>  支持远程信息传递 </td><tr><td>  活跃度和复杂度  </td>4
      </tr>  <tr>


 

<th rowspan="4">突现结构 </th>
<td>分类
<td> 微小突现（有意突现）  </td><td>  弱突现 </td><td> 多重突现  </td><td>  强突现</td>
      </tr>  <tr>
<td>结构特性
<td>系统组成部分  </td><td>  反馈循环 </td><td> 规模级别  </td>



</tr>
   </table>
 











## 第四章 内部经济##
<table>
    <tr>

<th rowspan="10"> 构成要素</th>
<td rowspan="2">资源</td>  <td>  有型资源  </td><td>  无形资源
    <tr>

<td> 抽象资源  </td><td> 具体资源  </td>
    <tr>
 <tr>

<td rowspan="1"> 实体  </td><td> 简单实体（属性）  </td><td>复合实体

<tr>

<th rowspan="4">循环机制 </th>
<td> 来源 </td><td> 消耗器  </td><td> 转换器</td><td> 交易器   </td>




</tr>
   </table>


<table>
    <tr>

<th rowspan="2"> 经济结构</th>
<td >负反馈引发均衡</td>  <td>  稳定随之间变化或周期性改变  </td><td><td>动态平衡，皮筋约束
<td rowspan="4">基于分数差的反馈 </th><td rowspan="4">长期投资vs短期收益 </td>
    <tr>

<td> 正反馈引发军备竞赛  </td><td> 指数曲线  </td><td> ①死锁和相互依赖②破坏性机制中下行螺旋  </td><td>微小的差异会放大
    <tr>
 <tr>



<tr>






</tr>
   </table>



<table>
    <tr>

<th rowspan="10"> 内部经济在游戏中的应用</th>
<td rowspan="1">补强物理机制</td>  <td> 金币、增益道具  </td>

<th rowspan="10"> 经济构建游戏的设计技巧</th><td  rowspan="2">不要一次把所有经济构建提供给玩家
    
 <tr>

<td rowspan="1"> 影响游戏进程  </td><td> 避免死锁（如不断重生资源）</td>
<tr>

<td rowspan="1">引入策略性玩法 </th>
<td> 长远规划和长远投资，使用时机 </td><td rowspan="2">留意超经济结构


<tr>

<td rowspan="3">创造大概率空间</th>
<td> 防止特定组合方案过于出众 </td>  
<tr>
<td> 概率空间足够大 </td>     <td  rowspan="2">利用地图产生变化性并限制概率空间           
<tr><td>多种方法过关 </td><tr>
</tr>
   </table>


</tr>
   </table>


*******


[返回主页](https://wqngqingyang.github.io/personal-blog/)
