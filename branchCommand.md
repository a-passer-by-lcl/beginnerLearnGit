#��֧����

*�г����б��ط�֧,��ǰ��֧ǰ����һ��*��
$ git branch

*�г�����Զ�̷�֧
$ git branch -r

*�г����б��ط�֧��Զ�̷�֧
$ git branch -a



*����һ���·�֧,����Ȼͣ���ڵ�ǰ��֧
$ git branch <branch-name>

*����һ���·�֧��ָ��ָ��commit
$ git branch <branch-name> <commit>

*����һ���·�֧����ָ����Զ�̷�֧����׷�ٹ�ϵ
$ git branch --track <branch-name> <remote-branch>



*�л���ָ����֧�������¹�����
$ git checkout <branch-name>

*�������л���ָ����֧����������������
$ git checkout -b <branch-name>



*�ϲ�ָ����֧����ǰ��֧
$ git merge --no-ff <branch-name>

ͨ��,�ϲ���֧ʱ,�������,Git����Fast forwardģʽ
������ģʽ��,ɾ����֧��,�ᶪ����֧��Ϣ

���Ҫǿ�ƽ���Fast forwardģʽ
Git�ͻ���mergeʱ����һ���µ�commit,�ӷ�֧��ʷ�ϾͿ��Կ�����֧��Ϣ

��ʾ����Fast forward
--no-ff����-

����Fast forward��ע��
$ git merge --no-ff -m "merge with no-ff" dev



*ѡ��һ��commit���ϲ�����ǰ��֧
$ git cherry-pick <commit>



*ɾ����֧
*�������û�кϲ���ʱ��ᵼ��ɾ��ʧ��
$ git branch -d <branch-name>

*��û�кϲ���ʱ��Ҳ��ɾ��
$ git branch -D <branch-name>

*ɾ��Զ�̷�֧
$ git push origin --delete <branch-name>
$ git branch -dr <remote/branch>



*�鿴��֧�ϲ�ͼ
$ git log --graph

�鿴��֧��ʷ
$ git log --graph --pretty=oneline --abbrev-commit



*����׷�ٹ�ϵ�������з�֧��ָ����Զ�̷�֧֮��
$ git branch --set-upstream <branch-name> <remote-branch>