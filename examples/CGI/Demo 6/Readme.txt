��� ���������� ������ ���������� ��������� � ���� "httpd.conf" ��������� ������:


RewriteEngine on 
RewriteCond %{HTTP:Authorization} ^(.*) 
RewriteRule ^(.*) - [E=HTTP_AUTHORIZATION:%1]


� ���� ��������� ������ ���� ������ ����: 

#LoadModule rewrite_module modules/mod_rewrite.so

�� �������� �� �� �����: 

LoadModule rewrite_module modules/mod_rewrite.so

� � ����� ������������� ���-������ Apache.

