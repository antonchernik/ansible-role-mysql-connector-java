Ansible Role for MySQL Connector/J
==================================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-mysql-connector-java.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-mysql-connector-java)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-mysql-connector-java.svg)](https://github.com/pantarei/ansible-role-mysql-connector-java)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-mysql-connector-java.svg)](https://github.com/pantarei/ansible-role-mysql-connector-java/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/5979.svg)](https://galaxy.ansible.com/detail#/role/5979)

Ansible Role for Ubuntu MySQL Connector/J Initialization.

Requirements
------------

This role require Ansible 1.9 or higher.

This role was designed for Ubuntu Server 14.04 LTS.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">parameter</th>
<th align="left">required</th>
<th align="left">default</th>
<th align="left">choices</th>
<th align="left">comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">mysql_connector_java_archive</td>
<td align="left">yes</td>
<td align="left">/tmp/mysql-connector-java-5.1.37.tar.gz</td>
<td align="left"></td>
<td align="left">Download archive filename for cache during (re)install.</td>
</tr>
<tr class="even">
<td align="left">mysql_connector_java_dest</td>
<td align="left">yes</td>
<td align="left">/tmp</td>
<td align="left"></td>
<td align="left">Destination directory where MySQL Connector/J .jar should install to.</td>
</tr>
<tr class="odd">
<td align="left">mysql_connector_java_jar</td>
<td align="left">yes</td>
<td align="left">mysql-connector-java-5.1.37-bin.jar</td>
<td align="left"></td>
<td align="left">MySQL Connector/J .jar filename for double check if installed to target directory correctly.</td>
</tr>
<tr class="even">
<td align="left">mysql_connector_java_sha256</td>
<td align="left">yes</td>
<td align="left">01e2f104c169863b4937a77045b008a372e5e254b803f69f030986167e626824</td>
<td align="left"></td>
<td align="left">Download archive sha256 checksum for cache during (re)install.</td>
</tr>
<tr class="odd">
<td align="left">mysql_connector_java_url</td>
<td align="left">yes</td>
<td align="left">http://cdn.mysql.com/Downloads/Connector-J/mysql-connector-java-5.1.37.tar.gz</td>
<td align="left"></td>
<td align="left">URL for download archive.</td>
</tr>
</tbody>
</table>

Dependencies
------------

-   [hswong3i.java](https://galaxy.ansible.com/detail#/role/5971)

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.java }
        - { role: hswong3i.mysq_connector_java, mysql_connector_java_dest: '/usr/share/jira/lib' }

License
-------

-   Code released under [MIT](https://github.com/hswong3i/ansible-role-mysql-connector-java/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

