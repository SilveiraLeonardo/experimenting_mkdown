# Product Report: Django-NV

Generated By Admin User (admin) on 12/23/2021 07:55PM UTC

Number of vulnerabilities found: 15

## VULNERABILITIES DESCRIPTION

### VULNERABILITY ID : 9

TITLE: Starting a Process With a Shell, Possible Injection Detected, Security Issue.

SEVERITY: High

RECOMMENDED TIME TO RESOLVE THE ISSUE: 30 days

DESCRIPTION: An SQL injection attack consists of insertion or “injection” of a SQL query via the input data given to an application. It is a very common attack vector. This plugin test looks for strings that resemble SQL statements that are involved in some form of string building operation. Unless care is taken to sanitize and control the input data when building such SQL statement strings, an injection attack becomes possible. If strings of this nature are discovered, a LOW confidence issue is reported. In order to boost result confidence, this plugin test will also check to see if the discovered string is in use with standard Python DBAPI calls execute or executemany. If so, a MEDIUM issue is reported.

FILE PATH: /src/taskManager/misc.py

LINE: 33

CODE:

```generic


32     # Let's avoid the file corruption race condition!
33     os.system(
34         "mv " +
35         uploaded_file.temporary_file_path() +
36         " " +
37         "%s/%s" %
38         (upload_dir_path,
39          title))
40 


```

USEFUL RESOURCES:

[https://bandit.readthedocs.io/en/latest/plugins/b608_hardcoded_sql_expressions.html](https://bandit.readthedocs.io/en/latest/plugins/b608_hardcoded_sql_expressions.html)

### VULNERABILITY ID : 15

TITLE: DL3018: Pin Versions in Apk Add. Instead of `Apk Add <package>` Use `Apk Add <package>=<version>`

SEVERITY: High

RECOMMENDED TIME TO RESOLVE THE ISSUE: 30 days

DESCRIPTION: Version pinning forces the build to retrieve a limited range of versions, or an exact particular version, regardless of what’s in the cache. This technique can also reduce failures due to unanticipated changes in required packages.

FILE PATH: /opt/Dockerfile

LINE: 9

USEFUL RESOURCES:

[https://github.com/hadolint/hadolint/wiki/DL3018](https://github.com/hadolint/hadolint/wiki/DL3018)

### VULNERABILITY ID : 16

TITLE: DL3042: Avoid Use of Cache Directory With Pip. Use `Pip Install --No-Cache-Dir <package>`

SEVERITY: High

RECOMMENDED TIME TO RESOLVE THE ISSUE: 30 days

DESCRIPTION: Once a package is installed, it does not need to be re-installed and the Docker cache can be leveraged instead. Since the pip cache makes the images larger and is not needed, it's better to disable it.

FILE PATH: /opt/Dockerfile

LINE: 10

USEFUL RESOURCES:

[https://github.com/hadolint/hadolint/wiki/DL3042](https://github.com/hadolint/hadolint/wiki/DL3042)

### VULNERABILITY ID : 11

TITLE: CVE-2021-30139 - (Apk-Tools, 2.10.4-r3)

SEVERITY: Medium

RECOMMENDED TIME TO RESOLVE THE ISSUE: 90 days

IMPACT: No impact provided

COMPONENT NAME: apk-tools - COMPONENT VERSION: 2.10.4-r3

MITIGATION: 2.10.6-r0

DESCRIPTION: In Alpine Linux apk-tools before 2.12.5, the tarball parser allows a buffer overflow and crash.

USEFUL RESOURCES:

[https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-30139](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-30139)

### VULNERABILITY ID : 12

TITLE: CVE-2021-36159 - (Apk-Tools, 2.10.4-r3)

SEVERITY: Medium

RECOMMENDED TIME TO RESOLVE THE ISSUE: 90 days

IMPACT: No impact provided

COMPONENT NAME: apk-tools - COMPONENT VERSION: 2.10.4-r3

MITIGATION: 2.10.7-r0

DESCRIPTION: libfetch before 2021-07-26, as used in apk-tools, xbps, and other products, mishandles numeric strings for the FTP and HTTP protocols. The FTP passive mode implementation allows an out-of-bounds read because strtol is used to parse the relevant numbers into address bytes. It does not check if the line ends prematurely. If it does, the for-loop condition checks for the terminator one byte too late.

USEFUL RESOURCES:

[https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-30139](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-30139)

### VULNERABILITY ID : 13

TITLE: CVE-2021-28831 - (Busybox, 1.31.1-r9)

SEVERITY: Medium

RECOMMENDED TIME TO RESOLVE THE ISSUE: 90 days

IMPACT: No impact provided

COMPONENT NAME: busybox - COMPONENT VERSION: 1.31.1-r9

MITIGATION: 1.31.1-r10

DESCRIPTION: decompress_gunzip.c in BusyBox through 1.32.1 mishandles the error bit on the huft_build result pointer, with a resultant invalid free or segmentation fault, via malformed gzip data.

USEFUL RESOURCES:

[https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-28831](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-28831)

### VULNERABILITY ID : 10

TITLE: Possible SQL Injection Vector Through String-Based Query Construction.

SEVERITY: Medium

RECOMMENDED TIME TO RESOLVE THE ISSUE: 90 days

DESCRIPTION: A SQL injection attack consists of insertion or “injection” of a SQL query via the input data from the client to the application. A successful SQL injection exploit can read sensitive data from the database, modify database data (Insert/Update/Delete), execute administration operations on the database (such as shutdown the DBMS), recover the content of a given file present on the DBMS file system and in some cases issue commands to the operating system. SQL injection attacks are a type of injection attack, in which SQL commands are injected into data-plane input in order to affect the execution of predefined SQL commands.

FILE PATH: /src/taskManager/views.py

LINE: 184

CODE:

```generic


183             curs.execute(
184                 "insert into taskManager_file ('name','path','project_id') values ('%s','%s',%s)" %
185                 (name, upload_path, project_id))
186 


```

USEFUL RESOURCES:

[https://owasp.org/www-community/attacks/SQL_Injection](https://owasp.org/www-community/attacks/SQL_Injection)

### VULNERABILITY ID : 14

TITLE: CVE-2020-28928 - (Musl, 1.1.24-r2)

SEVERITY: Low

RECOMMENDED TIME TO RESOLVE THE ISSUE: 120 days

IMPACT: No impact provided

COMPONENT NAME: musl - COMPONENT VERSION: 1.1.24-r2

MITIGATION: 1.1.24-r3

DESCRIPTION: In musl libc through 1.2.1, wcsnrtombs mishandles particular combinations of destination buffer size and source character limit, as demonstrated by an invalid write access (buffer overflow).

USEFUL RESOURCES:

[https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-28928](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-28928)

### VULNERABILITY ID : 17

TITLE: DL3059: Multiple Consecutive `RUN` Instructions. Consider Consolidation.

SEVERITY: Info

DESCRIPTION: Rationale: Each RUN instruction will create a new layer in the resulting image. Therefore consolidating consecutive RUN instructions will reduce the layer count (see https://docs.docker.com/develop/dev-best-practices/). In addition to that, each RUN runs in its own shell, which can be the source of confusion when part of a RUN instruction changes something about the environment, because these changes may vanish in the next RUN instruction. Drawbacks: Please review Docker's layer caching. In general you want layers first which don't change often, so they can be cached. Putting easy cacheable and non-cacheable commands in the same layer (by using one RUN command) might have negative performance issues. You might want to ignore this info level rule.

FILE PATH: /opt/Dockerfile

LINE: 10

USEFUL RESOURCES:

[https://github.com/hadolint/hadolint/wiki/DL3059](https://github.com/hadolint/hadolint/wiki/DL3059)

### VULNERABILITY ID : 18

TITLE: Hard Coded High Entropy In: test_all.py

SEVERITY: Info

IMPACT: This weakness can lead to the exposure of resources or functionality to unintended actors, possibly providing attackers with sensitive information or even execute arbitrary code.

MITIGATION: Secrets and passwords should be stored in a secure vault and/or secure storage.

FILE PATH: test_all.py

### VULNERABILITY ID : 19

TITLE: Hard Coded High Entropy In: truffleHog/truffleHog.py

SEVERITY: Info

IMPACT: This weakness can lead to the exposure of resources or functionality to unintended actors, possibly providing attackers with sensitive information or even execute arbitrary code.

MITIGATION: Secrets and passwords should be stored in a secure vault and/or secure storage.

FILE PATH: truffleHog/truffleHog.py

### VULNERABILITY ID : 20

TITLE: Hard Coded High Entropy In: tests.py

SEVERITY: Info

IMPACT: This weakness can lead to the exposure of resources or functionality to unintended actors, possibly providing attackers with sensitive information or even execute arbitrary code.

MITIGATION: Secrets and passwords should be stored in a secure vault and/or secure storage.

FILE PATH: tests.py

### VULNERABILITY ID : 21

TITLE: Hard Coded High Entropy In: truffleHog.py

SEVERITY: Info

IMPACT: This weakness can lead to the exposure of resources or functionality to unintended actors, possibly providing attackers with sensitive information or even execute arbitrary code.

MITIGATION: Secrets and passwords should be stored in a secure vault and/or secure storage.

FILE PATH: truffleHog.py

### VULNERABILITY ID : 22

TITLE: Hard Coded High Entropy In: Temp/Nothing

SEVERITY: Info

IMPACT: This weakness can lead to the exposure of resources or functionality to unintended actors, possibly providing attackers with sensitive information or even execute arbitrary code.

MITIGATION: Secrets and passwords should be stored in a secure vault and/or secure storage.

FILE PATH: temp/nothing

### VULNERABILITY ID : 23

TITLE: Hard Coded High Entropy In: secretFile.txt

SEVERITY: Info

IMPACT: This weakness can lead to the exposure of resources or functionality to unintended actors, possibly providing attackers with sensitive information or even execute arbitrary code.

MITIGATION: Secrets and passwords should be stored in a secure vault and/or secure storage.

FILE PATH: secretFile.txt
