
## "Recon on Career Portal - Misconfiguration Finding"

While practicing reconnaissance with dirsearch on Termux, I accidentally discovered a career portal of a large retail group that exposed several sensitive endpoints that should not be public (e.g., backup files, env files, upload paths,put path, admin path,js). Upon seeing 200/302 responses behind Cloudflare, I immediately stopped and did not attempt to access the content further, as it was out of scope and had no bug bounty program. Lesson learned: the importance of target filtering and ethics to know when to stop.

career . SOMETHING.JOB COM