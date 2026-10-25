
## "Recon on Career Portal - Misconfiguration Finding"

While practicing reconnaissance with dirsearch on Termux, I accidentally discovered a career portal of a large retail group that exposed several sensitive endpoints that should not be public (e.g., backup files, env files, upload paths,put path, admin path,js). Upon seeing 200/302 responses behind Cloudflare, I immediately stopped and did not attempt to access the content further, as it was out of scope and had no bug bounty program. Lesson learned: the importance of target filtering and ethics to know when to stop.


Conclusion: This portal should ideally have a bug bounty program to encourage responsible reporting. The findings suggest a lack of attention to detail from the development team in securing the production environment, leaving development artifacts exposed.

title : found lots of backdoor website 

target : career/[SOMETING]/ job .com
endpoint :found :env,put,upload,mysql.php,shell.php etc
proof:output dirsearch photo.zip
(https://github.com/urfemthings/web-recon-lots-of-backdoor/blob/main/output%20dirsearch%20photo.zip)
tools: dirsearch on termux
impact:Potential Information Disclosure - exposed files could leak internal server paths and configs

Recommendation: Remove sensitive files from prod, add WAF rules to block dev extensions, and implement a Bug Bounty program and recapca.

Note: Stopped immediately, no exploitation was performed.

