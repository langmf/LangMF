������ � CGI ��������� �� ������ ������ LangMF, ������������� ��� Apache �������� (WIN ���������).

��� ���������� ������ ����������:
 
 1) ���������� Apache ������:
 
	http://www.sai.msu.su/apache/httpd/binaries/win32/httpd-2.2.25-win32-x86-no_ssl.msi
    http://www.apachehaus.com/cgi-bin/download.plx
 
 2) ��������� � ���� "httpd.conf" ��������� ������:
  	
    # ALL LangMF Settings for Apache
    
    ScriptAlias /LMF/ "C:/Program Files/LangMF/"
    AddType application/x-httpd-mf .mf
    AddHandler mf-script .mf
    Action mf-script /LMF/LangMF.exe
    Action application/x-httpd-mf "/LMF/LangMF.exe"
    
    # for Apache v.2.4.x
    <Directory "C:/Program Files/LangMF/">
        Require all granted
    </Directory>
    
    # for Apache v.2.2.x
    <Directory "C:/Program Files/LangMF/">
        AllowOverride None
        Options None
        Order allow,deny
        Allow from all
    </Directory>
 
 3) ���������� LangMF � ���������� "C:/Program Files/LangMF/".

------------------------------------------------------------------------------
��� ������ ������ � cgi ������ �� �������������� ����� ���� � ���������� ����. ���� ������ ������������ 
����� ����������� �� ������� � "���� -> ���������" ����� �������� ��� "services.msc" � ������� "OK" ,����� 
� ����������� ���� ���� �� ������ �� ������� � ��������� "Apache2.2", ����� �� ��� ������ ������� ���� 
�������� �� "��������" ����� ������� �� ������� "���� � �������" � ��� ������ ������� 
"��������� �������������� � ������� ������". ��� �������� ������ ������������� Apache.
