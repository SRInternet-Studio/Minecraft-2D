# <div align="center">Minecraft 2D</div>

<p align="center">
 <img src="https://img.shields.io/badge/开发语言-Python-coral" alt="语言">
 <img src="https://img.shields.io/badge/核心库-Pygame-blue" alt="核心库">
 <a href="https://app.fossa.com/projects/git%2Bgithub.com%2FSRInternet-Studio%2FMinecraft-2D-for-LittleDream?ref=badge_shield&issueType=security" alt="FOSSA Status"><img src="https://app.fossa.com/api/projects/git%2Bgithub.com%2FSRInternet-Studio%2FMinecraft-2D-for-LittleDream.svg?type=shield&issueType=security"/></a>
</p>
 <div align="center">这是一款免费开源的2D沙盒游戏，玩家可以用方块搭建属于自己的世界</div>

## 详细信息

### 特点/功能
- 🧩玩家可以建造、破坏、修改游戏世界，使用游戏内的资源和工具进行创造。
- 🎮️自定义角色的属性，让角色可以行走和跳跃，用方块搭建2D跑酷游戏。
- 🪄自定义添加方块，添加其他的样式作为方块。
- 🎨物品栏及主物品栏，快速查找物品并选定物品。
- 🗒️聊天栏（输入一些指令，或在聊天栏上显示你输入的文字）。
- 📐数学函数绘图功能，可生成各种方程图像。

### 兼容性
- 支持 Win8及以上 操作系统
- **窗口大小建议**：最好不要小于 800x700，标准尺寸为 1200x700

## 如何使用

### 安装
1. 下载 [Releases](https://github.com/Minecows-Green/Minecraft-2D-for-LittleDream/releases) 中的安装程序,它是一个压缩包（···2D.zip）；
2. 解压文件，找到启动器 `MC--2D--Launcher.pyw`；
3. 双击启动程序。

### 如何使用源代码
1. 下载完源代码文件后解压缩；
2. 确保您的计算机已经安装了 **Python** 语言环境，如果未安装点击 [Python下载](https://www.python.org/) 进行安装。
3. 确保安装了**pip**，如果未安装请参考 [官方安装指南](https://pip.pypa.io/en/stable/installation/) 进行安装。
4. 下载依赖库，打开 **cmd** 依次键入以下代码：
 ```python
	 pip install pygame
	 pip install pygame.freetype
	 pip install pywin32
	 pip install wxPython
   ```
5. 运行主程序：`Minecraft--2D--画板.pyw`

## 游戏操作

### 1. 鼠标按键
- **左键** --------------------- 填充一个物体
- **滚轮** --------------------- 换物品（选定物品）
- **右键** --------------------- 放置一个物体

### 2. 键盘按键
- **W** ------------------------ 上移
- **S** ------------------------ 下移
- **A** ------------------------ 左移
- **D** ------------------------ 右移
- **Ctrl + W** ----------------- 加速上移
- **Ctrl + S** ----------------- 加速下移
- **Ctrl + A** ----------------- 加速左移
- **Ctrl + D** ----------------- 加速右移
- **Shift** -------------------- 前进
- **空格** --------------------- 后退
- **Esc** ---------------------- 返回
- **按住Z键 + 鼠标移动** ------- 连续填充物体
- **按住X键 + 鼠标移动** ------- 连续放置物体
- **<** ------------------------ 区块加载范围(+)
- **>** ------------------------ 区块加载范围(-)
- **E** ------------------------ 打开物品栏
- 搜索物品：输入物品代号后按回车键，将选定物品移到主物品栏
- **Q** ------------------------ 摧毁主物品栏的物品
- **T** ------------------------ 打开聊天栏
- **主键盘数字键1~9** ---------- 换物品（选定物品）
- **I** ------------------------ 显示表格
- **O** ------------------------ 隐藏显示信息
- **P** ------------------------ 隐藏物品栏

### 3. 指令集（输入后按回车键）

#### 基础指令
- **聊天**：直接输入文字，如 `Hello World!`
- **传送**：`/tp @a <x> <y>`，如 `/tp @a 114 514`
- **放置物体**：`/put <x1> <y1> <x2> <y2> id=<物品id>`，如 `/put 1 9 8 1 id=0114`
- **填充物体**：`/fill <x1> <y1> <x2> <y2>`，如 `/fill 1 9 8 1`
- **填充指定物体**：`/fill <x1> <y1> <x2> <y2> id=<物品id>`，如 `/fill 1 9 8 1 id=0114`
- **给予物品**：`/give @a id=<物品id>`，如 `/give @a id=0114`

#### 区块操作
- **复制区块**：`/copy name=<变量名> <x1> <y1> <x2> <y2>`，如 `/copy name=area 1 9 8 1`
  - 注：复制区块时最好放个方块在x1, y1，否则粘贴时会错位
- **粘贴区块**：`/glue name=<变量名> <x> <y>`，如 `/glue name=area 4 5`
- **列出复制区块**：`/list copy`
- **清除指定复制区块**：`/del copy name=<变量名>`，如 `/del copy name=area`
- **清除所有复制区块**：`/del copy`

#### 时间控制
- **更改时间**：`/time <时间> <参数>`，如 `/time 100 1`
  - 参数说明：0-默认，1-静止，2-向左流逝，3-向右流逝
- **更改时间流逝速度**：`/time.speed <速度>`，如 `/time.speed 1`
  - 速度范围：1~999

#### 角色控制
- **召唤角色**：`/character on <x> <y>`，如 `/character on 6 2`
- **关闭角色**：`/character off`
- **设置重力加速度**：`/character.g <重力>`，如 `/character.g 1.5`
- **设置跳跃初速度**：`/character.j <速度>`，如 `/character.j -24`
- **设置行走速度**：`/character.m <速度>`，如 `/character.m 10`
- **设置奔跑速度**：`/character.l <速度>`，如 `/character.l 20`

#### 数学函数绘图
- **基础用法**：`/plot <函数方程> <xmin> <xmax> <step>`，如 `/plot x**2 -10 10 1`
  - 使用默认选中方块（先通过鼠标滚轮或数字键选中一个方块）
- **指定方块ID**：`/plot <函数方程> --id=<方块ID> <xmin> <xmax> <step>`，如 `/plot math.sin(x) --id=0114 -20 20 1`
- **省略范围参数**：`/plot <函数方程> --id=<方块ID>`，如 `/plot math.cos(x) --id=0145`
  - 默认：xmin=-20, xmax=20, step=1

**注意事项**：
- 表达式中的数学函数需使用 `math.` 前缀，如 `math.sin(x)`、`math.sqrt(x)` 等
- 方块ID必须存在于资源文件中，否则生成后可能显示为缺失纹理
- 生成的方块位置基于世界坐标系整数格点，确保与现有方块对齐
- 若指定步长非整数，会被四舍五入为整数，建议使用整数步长

#### 其他指令
- **更改缩放比例**：`/scale.z <缩放比例>`，如 `/scale.z 72`

## 资源管理

### block 文件夹结构
- **building** --------- 建筑物品文件夹
- **circuit** ---------- 红石物品文件夹
- **other** ------------ 其他物品文件夹

### 自定义添加物品
1. 打开游戏根目录的 `block` 下三个子文件夹中的任意一个
2. 找到 `dic_block_image.dict` 文件并用记事本打开
3. 您会看到一个字典结构：`{'xxx.png': ['id', number], ...}`
   - `'xxx.png'` 是物品图片路径+图片名+后缀（键）
   - `['id', number]` 是物品ID和音效类型（值）
4. 添加新物品：`{'物品图片路径+图片名+后缀': ['定义物品id', 定义物品音效0~5]}`

### 物品音效对照表
- **0** ------ 无声
- **1** ------ 草的声音
- **2** ------ 木头的声音
- **3** ------ 沙子的声音
- **4** ------ 玻璃的声音
- **5** ------ 块的声音

## 游戏提示

1. **窗口大小**：游戏窗口大小最好不要小于 800x700，推荐使用标准尺寸 1200x700 以获得最佳体验
2. **物品栏使用**：使用E键打开物品栏，输入物品ID快速搜索和获取物品
3. **快速建造**：利用复制 `/copy` 和粘贴 `/glue` 指令可以快速建造复杂结构
4. **数学绘图**：使用 `/plot` 指令可以生成各种数学函数图像，如正弦波、抛物线等
5. **角色定制**：通过角色控制指令可以调整角色的各项属性，创造不同的游戏体验

<div align="center">
<br>
<img src='https://github.com/user-attachments/assets/5dfe6517-b6d3-4fc3-ab9f-40132ee8316e' alt='sr-ico' height="200" width="200"></img>
<img src='https://github.com/user-attachments/assets/2a0c7c1b-34f4-4b8c-9f85-55b02eb4437a' alt='sr-ico' height="200" width="200"></img>
	
<h2>Made by 思锐工作室</h2>
</div>
