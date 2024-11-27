# OpenGL 管线
## OpenGL管线
![opengl pipeline](../asset/blog/opengl_pipeline.png)
1. cpp获取GLSL代码，从文件中读取或硬编码为字符串
2. 创建着色器对象并将GLSL代码加载进着色器对象
3. opengl编译GLSL程序
### C++/OpenGL程序
1. 初始化GLFW库
2. 实例化GLFWWindow对象
3. 初始化GLEW库
4. 调用一次init()函数
5. 重复调用display()函数
