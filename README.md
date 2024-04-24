- 开发环境：vs2019或vs2022
- 使用的库：opencv，assimp（无需使用glfw，glad等），已包含在lib文件夹内

不需要配置其他的环境，因为没有使用glfw等库，也没有使用cuda加速，采用了openmp并行加速应是c++自带，无需额外配置

- 使用vs打开sln工程文件，重新生成解决方案，运行
由于主要在vs2022上开发，在vs2019或更低版本打开时，可能需要将工具集v143调到较低的版本

- 由于assimp库的使用，可能会提示缺失zlib.dll，
若缺失，可按照https://blog.csdn.net/LHXvs2015/article/details/120674525的步骤，下载解压zlib，用命令行工具nmake即可得到需要的文件

- 运行时，请用release（而不是debug），以开启openmp加速

- 交互方式：本程序会用光线追踪算法渲染两个自选材质的球体和一个手模型（或茶壶模型），
根据控制台的提示，依次输入数字来确定选择手还是茶壶模型、球1的材质、模型的材质、球2的材质，
随后根据控制台提示，输入光线的采样次数和反射次数，就会开始渲染，一段时间后会得到结果。

（参考：在开发者的电脑上，设置采样次数 100 反射次数 20 大约需要1分钟时间，所得结果的清晰度已经足够）


