   zkfire֮���Դ�1.0ֱ��������2.0 ����Ϊ2.0�汾��һ�������Ĺ��̣����ṩ�������ű�,֧��linux��windows����;��zkfire1.0ֻ��openfire���̴���ĵ�һ��jar��������ʱ������openfire������2.0�汾ȥ����openfire���ֳ���(�������ȥ����)����������zkfire1.0��Ⱥ��һЩbug��2.0��Ⱥ��ʵ�ַ�ʽ��1.0����һ�¡���ϸ˵���ɼ���http://www.oschina.net/p/zkfire��
   sbin�ļ�����linux��windows�������ű���
   zkfire�ļ�Ⱥ����zookeeper��������Ѿ���zookeeper���񡣿���ֱ�ӽ�zkfireָ�����е�zookeeper��������ȥ��zkfire����zk����:ע�͵�cluster.xml��zoo�ڵ㣻<zClient>127.0.0.1:3181</zClient> ָ��zk��ip��˿ڡ�����û�У�����԰�Ĭ�ϵ�����ָ������zk����

   �������zkfire��
   1,�������ݿ⡣��Ӧ��sql�ļ���database�У�ѡ����Ӧ���ݿ�ű����м��ɡ�
   2,�޸�ofproperty ������zkfire2.0Ҳ�����˼��������������ǲ��ֱ�����˵����

     xmpp.domain                 ���� Ĭ�� 127.0.0.1
     xmpp.socket.plain.port      ���ʶ˿� Ĭ��5222
     xmpp.proxy.port             ����˿� Ĭ��7777  ���ڴ����ļ��ȡ�
     xmpp.monitor.port(����)     ���ݶ˿� Ĭ��5915  
     xmpp.receipt.active(����)   ������������ͻ���֮�����Ϣ��ִ(�Զ�����Ϣ���ϻ���Э��) Ĭ��false������������ʱ��ͻ������,������Ϣ�����¼��������Ϣ��

   3,����conf/openfire.xml���������ݿ⡣��������openfire��openfire.xml��һ�µģ�����������������Բο�������openfire.xml���á�
   4,����conf/cluster.xml ��Ⱥ�ļ������÷�ʽ��zkfire1.0һ�¡��ɲο�http://www.oschina.net/p/zkfire.
   5,�����ű�sbin�ļ���zkfireStart.bat(windows) ,zkfireStart.sh (linux)

   
   http://127.0.0.1:5915/i ��ѯ�������������ݡ�(utf8����)
   http://127.0.0.1:5915/u ��ѯ�����û������ݡ�(utf8����)
      �����û������� ��Ⱥ���������������û�
      ���������û��� ��zkfire�����������û�


���κ�������黶ӭ��ʱemail����donnie4w@gmail.com��лл!
  