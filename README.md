### Hi there 👋

 <!--START_SECTION:waka-->
  <!--END_SECTION:waka-->
 name: Waka Readme

on:
  schedule:
    # Runs at 12am IST
    - cron: '30 18 * * *'
    # cron: '00 15 * * *'로 하면 한국 시간 기준으로 오전 12:00에 업데이트 된다
  workflow_dispatch:
jobs:
  update-readme:
    name: Update Readme with Metrics
    runs-on: ubuntu-latest
    steps:
      - uses: anmol098/waka-readme-stats@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ secrets.GH_TOKEN }}
          # 플래그 자리
