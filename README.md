一、简述
Medic3D是一个基于web的3D医疗数据可视化应用程序，支持显示3D网格模型(以OBJ文件的形式)以及3D体积数据，例如CT和MRI扫描(以MHR文件的形式)
应用程序支持用户之间的远程协作，用户可以共享数据、视图、注释，也可以通过集成聊天进行通信。
二、运行
Medic3D需要Node.js和MongoDB来运行。
如何安装依赖项，设置数据库并运行NodeJS应用程序？
$ # Setup database (do not forget to add path to MongoDB binaries to your PATH variable).
$ mkdir database
$ mongod --dbpath ./database
$ # Start server application.
$ cd src_server
$ node index.js
$ # Web application should be hosted on: <YOUR IP>:8080/web
三、主机托管
应用程序目前支持obj和raw的托管
# Host .obj mesh files by copying them in:
src_server/database_init_resources/obj
# Host .mhd/.raw volume files by copying them in:
src_server/database_init_resources/mhd
# Note: .mhd and .raw volume files must have a matching name
