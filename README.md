# Middlebury_v.2-_Evaluation

#    附件中是Middlebury v.2数据集的测试代码，Error_Non_31是测试非遮挡区域错误率的代码，其不仅可以测试Tsukuba, Venus, Teddy和Cones的错误率，还能测试其余27组Middlebury v.2立体匹配对的错误率。
#Test_Error_All测试全部区域的错误率。代码运行环境是Microsoft Visual Studio 2012/2013 + Opencv 2.4.8，全部31对立体匹配对的max disparity和scale在附件“Middlebury_Extended_31.txt”中，请一并下
#载。
#    Error_Non_31.zip压缩文件使用方式：1）解压缩文件至D盘根目录，用VS2013打开Error_Non_31.sln；2）配置OpenCV （我使用的是Opencv 2.4.8，其它版本应该也可以，但不要过低）；3）解压缩
#Error_Non_31.zip后里面有Data和Data_extended两个文件夹，其中Data文件夹中是Tsukuba,Venus,Teddy和Cones数据集，Data_extended是其余27组数据集；4）需要做的是把你得到的视差图放到对应的文件夹中去。例
#如Tsukuba的视差图分别命名为: tsukuba_dis.ppm, 放到D:\Error_Non_31\Data\tsukuba文件夹中，Venus, Teddy和Cones的前缀与Tsukuba一致。其余27组立体匹配对放到Data_extended文件夹中对应的文件中，例如
#Aloe命名为：_Aloe.ppm放到D:\Error_Non_31\Data_extended\Aloe文件夹中。
#    所有视差图的前缀和后缀（图像格式）均可修改，但为了使用方便，不建议修改程序。至于图像格式转换，我使用XnConvert软件对图像进行.pgm, .ppm, .png格式之间的转换，这款软件用百度搜索就可以搜到，使用
#起来非常方便。在测试完错误率之后，查看对应路径的文件夹（比如上述的D:\Error_Non_31\Data\tsukuba）可以得到非遮挡区域错误率的图像，其中非遮挡区域的错误像素用红色标记，错误率和代码运行出来的非遮挡错
#误率是一致的。
