#��֧����

	�г����б��ط�֧,��ǰ��֧ǰ����һ��*��
	$ git branch
	�г�����Զ�̷�֧
	$ git branch -r
	�г����б��ط�֧��Զ�̷�֧
	$ git branch -a
<br>
	����һ���·�֧,����Ȼͣ���ڵ�ǰ��֧
	$ git branch <branch-name>
	����һ���·�֧��ָ��ָ��commit
	$ git branch <branch-name> <commit>
	�������л���ָ����֧����������������
	$ git checkout -b <branch-name>
	����һ���·�֧����ָ����Զ�̷�֧����׷�ٹ�ϵ
	$ git branch --track <branch-name> <remote-branch>
	�л���ָ����֧�������¹�����
	$ git checkout <branch-name>
<br>
	�ϲ�ָ����֧����ǰ��֧
	$ git merge --no-ff <branch-name>
	ѡ��һ��commit���ϲ�����ǰ��֧
	$ git cherry-pick <commit>
<br>
	ɾ����֧,�������û�кϲ���ʱ��ᵼ��ɾ��ʧ��
	$ git branch -d <branch-name>
	��û�кϲ���ʱ��Ҳ��ɾ��
	$ git branch -D <branch-name>
	ɾ��Զ�̷�֧
	$ git push origin --delete <branch-name>
	$ git branch -dr <remote/branch>
<br>
	�鿴��֧�ϲ�ͼ
	$ git log --graph
	����׷�ٹ�ϵ�������з�֧��ָ����Զ�̷�֧֮��
	$ git branch --set-upstream <branch-name> <remote-branch>