#SelfHealing#
    ����zabbix ������Ϣȥ���崦�������Զ�����������

# ����Ҫ��:
    python 2.7 �汾
    mysql 5.6����

# ��װ������:
    pip install -r requirements.txt

# ʹ�÷�����

1. **zabbix����ģ��**
    ```
    �澯����:{HOST.NAME}
    �澯IP:{HOST.IP}
    �澯ʱ��:{EVENT.DATE}{EVENT.TIME}
    �澯�ȼ�:{TRIGGER.SEVERITY}
    �澯��Ϣ: {TRIGGER.NAME}
    �澯��Ŀ:{TRIGGER.KEY1}
    ��������:{ITEM.NAME}:{ITEM.VALUE}
    ��ǰ״̬:{TRIGGER.STATUS}:{ITEM.VALUE1}
    �¼�ID:{EVENT.ID}
    ```

2. **cp db.conf.demo db.conf**��
    ```
    ���cmdb �ʲ����ݿ�������Ϣ������Ŀ����jumpserver �ʲ��ɼ���Ϣȥƥ�䡣
    [dbconfig]
    db = jumpserver
    host = ip
    user = user
    passwd = password
    charset = utf8
    timeout = 600

    [DingURL]
    DingURL1 = your dingding
    DingURL2 = your dingding
    ```


3. **��Կ�ļ�**
      ```
      ��keys Ŀ¼����,���û��������Ŀ��Ŀ¼����keys Ŀ¼��Ȼ�������������˽Կ�ļ��������Ŀ¼������Ϊid_rsa����Ȩ600��������ȨΪ600 ������޷�����Զ��������
      ```

4. **supervisor**

      �ο�supervisor Ŀ¼���������ļ�ȥ��������

5. **��������**
    ```
     �ӿ��ļ� SelfHealing.py
     ���Զ��Ĵ��ļ���ȡ���嶯��,���������playbookȥ���ƶ�����
    ```

5. **��������**
    ```
     python AutoPlay.py
    ```





