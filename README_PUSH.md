Instructions to push updates to GitHub (choose one):

1) If you use SSH and have your key set up locally:
   cd /tmp/ravikm-phd.github.io
   git add .
   git commit -m "Add blog pages and styles"
   git push origin main

2) If you want to use a PAT temporarily (less recommended):
   You can set the origin url with the token embedded for one push only:
   git remote set-url origin https://<TOKEN>@github.com/ravikm-phd/ravikm-phd.github.io.git
   git push origin main
   # Then immediately remove token from remote:
   git remote set-url origin https://github.com/ravikm-phd/ravikm-phd.github.io.git
   # Revoke the PAT in GitHub settings when done.

3) Using GitHub CLI (recommended):
   gh auth login
   gh repo view ravikm-phd/ravikm-phd.github.io --web
   # or simply git push if gh auth configured

After pushing, go to the repo → Settings → Pages, ensure branch 'main' is selected, wait for the HTTPS certificate (may take a few minutes), and enable 'Enforce HTTPS'.

DNS: for privability.works at Name.com, add A records to 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 for the apex, and a CNAME for 'www' pointing to ravikm-phd.github.io.
