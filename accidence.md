#Git����

###1��Git���
* Git��Ŀǰ���������Ƚ��ķֲ�ʽ�汾����ϵͳ��
* Git��һ���ֲ�ʽ�İ汾����ϵͳ�������Linus Torvalds��д������Linux�ں˴���Ĺ���
* GitHub ʹ�� git �ֲ�ʽ�汾����ϵͳ���� git ����� Linus Torvalds Ϊ����Linux����������ģ�����Ե��� Linux ƽ̨����Windows��Щì�ܣ�����GitHub ������GitHub for Windows��Ϊ Windows ƽ̨�������ṩ��һ������ʹ�õ� Git ͼ�οͻ��ˡ�

###2������Git�ֿ�
1. ע���˻��Լ������ֿ�
	* ��½[Github](https://github.com/)ע��Github�˺�--[ע��](http://wiki.jikexueyuan.com/project/github-basics/sign-up.html)
	* [�����ֿ�](http://wiki.jikexueyuan.com/project/github-basics/creat-new-repo.html)������û�ֻ�ܽ������ֿ⣩

2. ��װ�ͻ���msysGit
	* Windows�û��Ƽ�[msysGit](https://git-for-windows.github.io/)
	Github�Ƿ���ˣ�Ҫ�����Լ�������ʹ��Git����Ҫһ��git�ͻ���
	* Windows�û��Ƽ�[msysGit](https://git-for-windows.github.io/)
	* [msysGit��װ�̳�](http://jingyan.baidu.com/article/e52e36154233ef40c70c5153.html)
	* װ��msysgit���Ҽ���꣬�ڱ��زֿ����Ҽ�ѡ��Git Init Here��������һ��.git�ļ��У���ͱ�ʾ����git�����ɹ���

3. ����Git
	* Ҫ�ڱ�������msysGit���Լ�Զ�̵�Github�ֿ⣬��Ҫ��������һϵ������
	* �ڱ��زֿ����Ҽ�Git Bash����git�����У�����ȫ����������û���������
		* $ git config --global user.name "your name"
		* $ git config --global user.email "your-email@youremail.com"

	* ���ڱ���Git�ֿ��GitHub�ֿ�֮��Ĵ�����ͨ��SSH���ܵģ�����SSH Key
	* ���û���Ŀ¼�£�������û��.sshĿ¼������У��������Ŀ¼����û��id_rsa��id_rsa.pub�������ļ�������Ѿ����ˣ���ֱ��������һ��
	* ���û���������������У�����yes,һ·�س�
		* $ ssh-keygen -t rsa -C "your-email@youremail.com"

	* id_rsa��id_rsa.pub�ļ�SSH Key����Կ�ԣ�id_rsa��˽Կ������й¶��id_rsa.pub�ǹ�Կ���ɸ����κ���

	* ��¼Github��[����SSH Key](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001374385852170d9c7adf13c30429b9660d0eb689dd43a000)
	* ��֤�Ƿ�ɹ������������� $ ssh -T git@github.com

4. ���Զ�ֿ̲⣬�����Github�ϵĲֿ�û��README.md�ļ�ʱ�����������ֿ�ʱ�㲻ѡ��Initialize this repository with a README
	* $ git remote add origin git@github.com:yourName/yourRepo.git
		* yourName-----------���Github�û���
		* yourRepo-----------���Github�ϵĲֿ�

5.�ύ���ϴ�
* $ git add <files>-----------------------����ļ����ϴ����ݴ���
$ git status------------------------------�鿴����Щ�޸�
* $ git commit -m "<message>"-------------�ϴ�����֧
* $ git push origin master----------------�����زֿ����͵�Զ�ֿ̲�


