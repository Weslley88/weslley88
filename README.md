## Olá! Eu sou o Weslley!

- 🔭 Hoje estou a procura de uma vaga de Desenvolvedor Front-End
- 🌱 Tenho conhecimento em HTML5, CSS3, JavaScript, React e MySQL
- 😄 Pronouns: ele/dele

<div>
  <a href="https://github.com/weslley88">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=weslley88&show_icons=true&theme=dark&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=weslley88&layout=compact&langs_count=7&theme=dark"/>
</div>
  
<div style="display: inline_block"><br>
  <img align="center" alt="Weslley-Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
  <img align="center" alt="Weslley-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Weslley-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">  
  <img align="center" alt="Weslley-MySQL" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original.svg">   
  <img align="center" alt="Weslley-Debian" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/debian/debian-plain.svg">
 
  ##
  
  <a href="https://www.linkedin.com/in/weslleyosilva88" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>
  <a href = "mailto:weslley.os88@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a> 

</div>
  
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: weslley88
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
