������ � CGI ��������� �� ������ ������ LangMF.

------------------------------------------------------------------------------
��� ���������� ������ ��� �������� Apache ����������:

 1) ���������� Apache ������:

    https://www.apachehaus.com/cgi-bin/download.plx

 2) ��������� � ���� "httpd.conf" ��������� ������:

    # LangMF Settings

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


------------------------------------------------------------------------------
��� ���������� ������ ��� �������� lighttpd ����������:

 1) ���������� lighttpd ������:

    http://lighttpd.dtech.hu

 2) ��������� � ���� "lighttpd.conf" ��������� ������:

    # LangMF Settings
    server.modules = ("mod_access", "mod_accesslog", "mod_cgi")
    static-file.exclude-extensions = ( ".mf" )
    cgi.assign = (".mf" => "c:/Program Files/LangMF/LangMF.exe" )


------------------------------------------------------------------------------
��� ������ ������ � cgi ������ �� �������������� ����� ���� � ���������� ����. ���� ������ ������������ 
����� ����������� �� ������� � "���� -> ���������" ����� �������� ��� "services.msc" � ������� "OK" ,����� 
� ����������� ���� ���� �� ������ �� ������� � ��������� "Apache2.4" ��� "lighttpd", ����� �� ��� ������ ������� ����,
�������� �� "��������" ����� ������� �� ������� "���� � �������" � ��� ������ ������� 
"��������� �������������� � ������� ������". ��� �������� ������ ������������� ������.
