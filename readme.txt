  zkfire = zookeeper+openfire(3.8.1)
  openfire http://www.igniterealtime.org/
  Openfire ����Java��������Դ��ʵʱЭ����RTC������������XMPP��Jabber��Э��,������ʹ�������׵Ĺ�����Ч�ʵļ�ʱͨ�ŷ�����. 
  ���ݶ�xmpp��openfire����⣬����openfire����Ӧ�ĵط�ֲ�������Ĵ��룬����zookeeper��Ҳһ�������zkfire�С�ʹ��zookeeper(http://zookeeper.apache.org/)����Ⱥ�еĽڵ㡣
  �ͻ���½��Ⱥ�еĲ�ͬ����������ͨ�ž����½ͬһ̨������һ����
  openfire����Ҳ��һ�׼�Ⱥ��ʵ�֣�ʹ����oracle ��coherence���м����ʹ��ʱҪ�Լ�������Ӧ��jar���뼯Ⱥ�����
  ֮�������Լ�������һ�׼�Ⱥʵ�֣�һ���Ǹ���Ⱥ�ṩ��һЩѡ��һ������Ȥ^_^��
  
  zkfireʹ�õĳ�����
  zkfire����zookeeper�ķ�����������ͻ������ӳ��򣬵����Բ����������zookeeper���񣬿�����openfire֮�����⿪������zookeeper���񣬴�ʱֻ��ָ��
  cluster.xml�����ļ���zClient�ڵ�����ӵ�ַ���ɡ�
  ���ֻ��zookeeper����������ô����openfire������ֻ��Ҫ����ͬһ��zookeeper�������Ϳ������openfire�ļ�Ⱥ
  �����zookeeper��Ⱥ������zookeeper�ļ�Ⱥ�ص㣬��Ⱥ�нڵ㲻Ӧ������3̨���������һ���zk�ڵ�崻�����ô������Ⱥ�������������Ĺ�����
  
  ʹ�÷�����
  ��zkfire.jar���滻lib�µ�openfire.jar,֮��������zkfire.jarֻ��Ϊ���������֣����ֿ�������ȡ������cluster.xml�ŵ�binĿ¼�¡�
  zkfire���ڵ�openfire��ʵ�֣��������ʹ�õĻ����鲻Ҫ����openfire����ļ�Ⱥ���ܡ�
  �ڰ�װ��openfireĿǰbin�£�����cluster.xml�ļ���
  ʾ���������£�
  <?xml version="1.0" encoding="UTF-8"?>
   <jive>
        <!-- �ýڵ�����openfire������֮��ͨѶ��IPΪ����IP��ַ���������������ܷ��ʵ� -->
	<notice>10.10.152.180:3004</notice>
         <!-- zoo�ڵ���������zkfire��zookeeper�������������zk����������ô����ڵ����ȥ����-->
	<zoo> 
		<tickTime>2000</tickTime>
		<initLimit>10</initLimit>
		<syncLimit>5</syncLimit>
		<dataDir>E:/zoo/data</dataDir>
		<clientPort>3181</clientPort>
		<server name="server.1">10.10.152.180:2888:3888</server>
              <server name="server.2">10.10.152.185:2888:3888</server>
              <server name="server.3">10.10.152.189:2888:3888</server>
		<myid>1</myid>
		<!-- ########## -->
		<globalOutstandingLimit>1000</globalOutstandingLimit>
	</zoo>
        
      <!-- �ýڵ���������zk���������������zkfire�����zk����������ô�ýڵ����ȥ�� -->
	<zClient>127.0.0.1:3181</zClient>
   </jive>

   zoo�еĽڵ�server��������zookeeper�ļ�Ⱥ��myidָ������zookeeper��������myidֵ��server.X ������־��Ƕ�Ӧmyid�е����֣���Ⱥ�в�ͬzk��������myidֵ��ͬ��
   zoo�������ڵ�����ݽԶ�Ӧzk�����ļ��ļ�ֵ���ݡ����ﲻ�����������Բο� http://rdc.taobao.com/team/jm/archives/665����dataDir��clientPort�Ǳ������ã�����ָ��zookeeper�����ļ���ַ������˿ڡ� 
  