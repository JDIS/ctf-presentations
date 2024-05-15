---
marp: true
theme: gaia
class: invert

---

# Bash
![bg right:25% contain](../Images/logo_jdis.png)
<style scoped>h1 {font-size: 300%;position:absolute; margin:25% 0;}</style>

---
# Recherche dans les fichiers

``` rgrep ``` : une meilleure facon que ``` cat foo | grep ``` 


<!-- paginate: true -->



---
# Curl

curl -X POST -d 'api_dev_key=UZlSQ5uqgyipMGp4KPADebiSDVrPsYhZ' -d 'api_user_key=22488329c4577b4182268fadf7801dda' -d 'api_option=show_paste' -d 'api_paste_key=j1Y2Hbva' "https://pastebin.com/api/api_post.php"

curl -X POST -d 'api_dev_key=UZlSQ5uqgyipMGp4KPADebiSDVrPsYhZ' -d 'api_user_key=22488329c4577b4182268fadf7801dda' -d 'api_option=show_paste' -d 'api_paste_key=CXeiUeLV' "https://pastebin.com/api/api_post.php"

curl -X POST -d 'api_dev_key=UZlSQ5uqgyipMGp4KPADebiSDVrPsYhZ' -d 'api_user_key=22488329c4577b4182268fadf7801dda' -d 'api_option=list' -d 'api_results_limit=100' "https://pastebin.com/api/api_post.php"