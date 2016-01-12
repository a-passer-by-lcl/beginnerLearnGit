#��֧����

###һ������֧master
    1����������ҽ���һ������֧����master��֧

    2������֧����������ĳ����������ʽ�汾�ģ����ṩ���û��汾(1.0, 2.0...)

    3��git����֧�����֣�Ĭ�Ͻ���master���������Զ������ģ��汾���ʼ���Ժ�Ĭ�Ͼ���������֧�ڽ��п���

###����������֧develop
    1���ճ�������develop��֧�Ͻ��У��������õķ�֧������develop

    2�����Ҫ���ⷢ����Ҫ��master��֧����develop��֧���кϲ�(merge)

    3��develop��֧Ҫ������֧master(������)

    4��������֧develop����
		(1)������dev��֧
		$ git branch dev master
		(2)���л���dev�ϲ�
		$ git checkout dev
		���ߴ������л�
		$git checkout -b <branchName>

		(3)���鿴��֧
		$ git branch

		(4)����dev��֧���п�������
		$ git add <filename>
		$ git status
		$ git commit <filename> -m <message>

		(5)���л���master��֧
		$ git checkout master

		(6)����dev��֧�ϲ���master��֧
		$ git merge --no-ff dev

		(7)��ɾ��dev��֧
		$ git branch -d dev

		(8)���鿴�ϲ�ͼ
		$ git log --graph
����
###������ʱ�Է�֧
    1���汾����Ҫ��������Ҫ��֧����������֧master�뿪����֧develop

    2����������Ҫ��֧�⻹������ĳЩ�ض�Ŀ�ĵİ汾����������ʱ��֧

    3����ʱ��֧��Ҫ�����֣��������ܷ�֧-feature��Ԥ������֧-release���޲�bug��֧-fixbug

###�ġ����ܷ�֧-feature
    1�������ڿ���ĳЩ�ض����ܣ��ӿ�����֧develop�ֳ���֧��֧��������ɺ��ٲ��뿪����֧develop

    2�����ܷ�֧feature������ʽ��feature-*

    3������һ�����ܷ�֧
		(1)�������л������ܷ�֧
		$ git checkout -b feature-x develop

		(2)������ɺ󣬽����ܷ�֧�ϲ���develop��֧
		$ git checkout develop
		$ git merge --no-ff feature-x

		(3)ɾ��feature��֧
		$ git branch -d feature-x

###�塢Ԥ������֧-release
    1����ָ������ʽ�汾֮ǰ�����ϲ���master��֧֮ǰ����Ԥ�����İ汾���в���

    2��Ԥ������֧�ӿ�����֧develop�Ϸֳ���֧��֧��Ԥ���������Ժ󣬱���ϲ���������֧develop������֧master��

    3��Ԥ������֧release������ʽ��release-*

	4������һ��Ԥ������֧
		(1)�������л���Ԥ������֧
		$ git checkout -b release-1.0 develop

		(2)����󣬺ϲ���master��֧
		$ git checkout master
		$ git merge --no-ff release-1.0

		(3)�Ժϲ����ɵ��½ڵ㣬��һ����ǩ
		$ git tag -a 1.0

		(4)�ٺϲ���develop��֧
		$ git checkout develop
		$ git merge --no-ff release-1.0

		(5)ɾ��Ԥ������֧
		$ git branch -d release-1.0

###�����޲�bug��֧-fixbug
    1����������ʽ�汾��������bug������bug�޲��ķ�֧

    2���޲�bug��֧�Ǵ�����֧master�Ϸֳ����ġ��޲������Ժ��ٺϲ���master��develop��֧���������������Բ���fixbug-*����ʽ��


    3���޲�bug��֧fixbug������ʽ��fixbug-*

    4������һ���޲�bug��֧
	    (1)�������л����޲�bug��֧
		$ git checkout -b fixbug-0.1 master

	    (2)�޲�bug��ɺ󣬺ϲ�������֧master��
		$ git checkout master
		$ git merge --no-ff fixbug-0.1
		$ git tag -a 0.1.1

	    (3)�ٺϲ���������֧develop��
		$ git checkout develop
		$ git merge --no-ff fixbug-0.1

		(4)ɾ���޲�bug��֧
		$ git branch -d fixbug-0.1

    5��������bug��Ҫ�޸ģ������ڹ�����û�����ʱ���Ȱ����ڵķ�֧�������������·�֧���޸�bug�����ҵ����صķ�֧�������

		(1)�ѵ�ǰ�����ֳ������ء�����,���Ժ�ָ��ֳ����������
		$ git stash

		(2)�л���mester��֧
		$ git checkout master

		(3)����bug��֧
		$ git checkout -b fixbug-0.1 master

		(4)�ύbug��֧����ɾ��
		$ git checkout master
		$ git merge --no-ff fixbug-0.1
		$ git branch -d fixbug-0.1

		(5)�鿴������
		$ git status

		(6)�鿴������Ĺ����ֳ�
		$ git stash list

		(7)�ָ�������Ĺ����ֳ�
		$ git stash apply----�ָ���stash���ݲ���ɾ��������Ҫ��git stash drop��ɾ��(���Ƽ�ʹ��)
		$ git stash pop-----�ָ���ͬʱ��stash����Ҳɾ����

		(8)���stash,�ָ���ʱ��
		$ git stash list

		(9)�ָ�ָ����stash
		$ git stash apply stash@{0}