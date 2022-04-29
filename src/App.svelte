<script>
  import { countdown } from "./countdown.min.js";
  import IconButton from "./IconButton.svelte";

  let timespan;
  countdown(function (ts) {
    // console.log(ts);
    timespan = ts;
  }, new Date(2022, 3, 30));
</script>

<div id="bg">
  <div id="photos-bg">
    <div id="photos" class="unselectable">
      {#each Array(55) as _, i}
        <img src="./img_resized/{i + 1}.jpg" alt="a{i + 1}" />
      {/each}
    </div>
  </div>
  <main>
    <h1 id="title">限縮檢舉倒數</h1>
    <section class="center">
      <div id="countdown">
        <div>
          <div class="digit">
            {timespan.days.toString().padStart(2, "0")}
          </div>
          <span>天</span>
        </div>
        <div>
          <div class="digit">
            {timespan.hours.toString().padStart(2, "0")}
          </div>
          <span>時</span>
        </div>
        <div>
          <div class="digit">
            {timespan.minutes.toString().padStart(2, "0")}
          </div>
          <span>分</span>
        </div>
        <div>
          <div class="digit">
            {timespan.seconds.toString().padStart(2, "0")}
          </div>
          <span>秒</span>
        </div>
      </div>
    </section>
    <section id="article">
      <h1>一分鐘了解什麼是限縮檢舉</h1>
      <h3>什麼是交通違規檢舉？</h3>
      <p>
        在我國<a
          href="https://law.moj.gov.tw/LawClass/LawAll.aspx?pcode=K0040012"
          >道路交通管理處罰條例</a
        >中有規定，民眾可以針對道路違規行為向警察機關檢舉，最初這項規定是為了彌補警力不足和嚇阻民眾，並設有獎金，因此有人以檢舉當作工作，被稱為「檢舉達人」。
      </p>
      <h3>現在檢舉有獎金嗎？</h3>
      <p>
        時過境遷，現今檢舉交通違規已經沒有獎金，並且還要實名檢舉，但近年檢舉量是不減反增，可以發現檢舉達人並不是為了獎金。
      </p>
      <h3>檢舉真的能夠改善交通嗎？</h3>
      <p>
        目前沒有相關研究，因此沒有定論。如果家裡附近充滿違規停車，那麼檢舉可能是清空違停的最佳手段了。
      </p>
      <h3>為什麼需要檢舉？</h3>
      <p>
        民國85年立法新增檢舉管道，目的是為了彌補警力和嚇阻民眾，然而檢舉會造成檢舉人與違規人與警察間的對立、民眾檢舉的品質良莠不齊、設備未經檢驗等，不是一個改善交通的理想方法，我國其實設有<a
          href="https://law.moj.gov.tw/LawClass/LawAll.aspx?pcode=D0080061"
          >交通助理人員管理辦法</a
        >，經過專業訓練的交通助理人員可以負責稽查違規行為，不需要民眾檢舉。遺憾的是，我國交通助理人員並不多。
      </p>
      <h3>限縮檢舉是什麼？</h3>
      <p>
        民國110年由陳歐珀等19人提案修法，將原本的道路交通管理處罰條例的違規項目限縮到46件，並將在民國111年4月30日正式實施。修法後只有<a
          href="https://www.moto7.net/2021/12/law-violation-report.html"
          >正面表列的46項才可以檢舉</a
        >，其中<b>並不包含</b>：
      </p>
      <ul>
        <li>變造車牌</li>
        <li>違規停車</li>
        <li>胎紋不足</li>
        <li>人行道上停車</li>
        <li>跨越兩車道行駛</li>
        <li>行人穿越道上停車</li>
        <li>轉彎車不讓直行車</li>
        <li>...</li>
      </ul>
      <p>
        立委說限縮檢舉是為了減緩員警壓力，然而人行道上有車擋路怎麼辦？交通部：報案請警察處理。
      </p>
      <h3>4/30以後，會怎麼樣？</h3>
      <p>
        民眾除了46項以外都不能檢舉，其他違規項目必須要由警察處理，也就是餐車可以隨便停車生意也不用怕檢舉魔人，紅線和黃線和白線會變成同一種線，也就是停車線。4/30以後，台灣的停車問題會獲得解決，因為大部分的路邊都會變成免費停車場。
      </p>
      <h3>違規停車不會怎樣吧？</h3>
      <p>
        請仔細看網頁背景圖，很多違停造成死亡的案例，違停影響到行車視野、增加道路不確定性，會對其他用路人造成危險。
      </p>
      <h3>說實話，這很重要嗎？</h3>
      <p>
        台灣至今COVID-19的總死亡人數為860人，然而因為交通事故而死的人數是每年3,000人，台灣的路甚至比病毒還可怕，或許病毒跟交通事故不能互相比較，那麼以日本為例，日本的總人口約1億人，台灣的總人口約2,300萬人，日本去年的交通事故死亡人數一樣是3,000人，總人口為台灣數倍的國家死亡人數卻一樣，代表台灣的道路不安全。
      </p>
      <hr />
      <h1>民眾檢舉交通違規的修法歷史</h1>
      <div class="vtl">
        <div class="event">
          <p class="date">
            民國85年：增訂七條之一
            <IconButton
              title="立法院議案關係文書院總第756號政府提案之3690號"
              link="https://lis.ly.gov.tw/lgcgi/lgmeetimage?cfcec7cbcecbcfcfc5cdc8d2cac7"
              icon="bi bi-box-arrow-up-right"
            />
          </p>
          <h4>第7-1條</h4>
          <p class="txt">
            對於違反本條例之行為者，民眾得敘明違規事實或檢具違規證據資料，向公路主管或警察機關檢舉，經查證屬實者，應即舉發。
          </p>
          <h4>修法理由</h4>
          <p class="txt">
            由於警力有限及民眾取巧違規成性，為交通秩序混亂原因之一，民眾如能利用適當管道檢舉交通違規，除可<b
              >彌補警力之不足</b
            >外，亦將產生極大之嚇阻效果，爰增訂本條。
          </p>
        </div>
        <div class="event">
          <p class="date">
            民國91年：法律保留
            <IconButton
              title="立法院議案關係文書院總第732號政府提案之8467號"
              link="https://lis.ly.gov.tw/lgcgi/lgmeetimage?cfcacfcecfcacfcbc5ced2cccbcd"
              icon="bi bi-box-arrow-up-right"
            />
          </p>
          <h4>修法理由</h4>
          <p class="txt">
            現行違反道路交通管理事件統一裁罰標準及處理細則第二十三條得逕行舉發之規定，因影響人民權利義務，為符合法律保留之精神，爰酌予修正增訂於本條。
          </p>
        </div>
        <div class="event">
          <p class="date">
            民國94年：明文科學儀器可舉發行為
            <IconButton
              title="立法院議案關係文書院總第756號委員提案之5782號"
              link="https://lis.ly.gov.tw/lgcgi/lgmeetimage?cfc9cfcecfcdcfcec5ccc7d2c7c7"
              icon="bi bi-box-arrow-up-right"
            />
          </p>
        </div>
        <div class="event">
          <p class="date">
            民國103年：修法限制連續檢舉
            <IconButton
              title="立法院議案關係文書院總第756號委員提案之15628號之1"
              link="https://lis.ly.gov.tw/lgcgi/lgmeetimage?cfc7cfcacecdc8c6c5cecaccd2cecac9"
              icon="bi bi-box-arrow-up-right"
            />
          </p>
          <h4>第7-1條</h4>
          <p class="txt">
            對於違反本條例之行為者，民眾得敘明違規事實或檢具違規證據資料，向公路主管或警察機關檢舉，經查證屬實者，應即舉發。但行為終了日起逾七日之檢舉，不予舉發。
          </p>
          <h4>修法理由</h4>
          <p class="txt">
            為避免檢舉人刻意鑽營法律文字，造成法條之目的逸失，甚至衍生社會、鄰里之不安與不和諧，同時保障法條原立法精神目的在維護交通、保障安全，故針對舉發部分，擬定期限之規定，可強化社會秩序之安定性。
          </p>
        </div>
        <div class="event">
          <p class="date">
            民國108年：391萬件民眾檢舉，實際舉發299萬件
            <IconButton
              title="立法院公報 第 109 卷 第 48 期 委員會紀錄"
              link="https://lis.ly.gov.tw/lgcgi/lypdftxt?xdd!cec9cacececac7c7cbcb81cecfc6cfcbc7cfcec4cfcccfcfc4cfcccbc7"
              icon="bi bi-box-arrow-up-right"
            />
          </p>
          <h4>第7-1、7-2、85-1條修法提案說明</h4>
          <p class="txt">
            鄭委員正鈐：那全年度開的紅單總共有多少件？<br />
            王組長鳳輝：大概一千二百多萬件。<br />
            鄭委員正鈐：民眾檢舉開單占所有開單量的幾趴？<br />
            王組長鳳輝：<b>三分之一</b>。
          </p>
          <p class="txt">
            陳委員歐珀：..其實共同要面對的問題就是民眾檢舉的交通處罰要如何處理。本席在去年就提出這個修正草案，當時曾引發社會的熱論，大家也認為說這個確實是我們臺灣社會上所存在的一種很特殊的狀況。我們去瞭解之後發現，<b
              >世界上透過民眾檢舉作成處分的案子的國家也不多</b
            >...
          </p>
        </div>
        <div class="event">
          <p class="date">
            民國110年：將可檢舉之道交條例違規行為限縮至46項
            <IconButton
              title="立法院公報 第 109 卷 第 48 期 委員會紀錄"
              link="https://lis.ly.gov.tw/lgcgi/lypdftxt?xdd!cec9cacececac7c7cbcb81cecfc6cfcbc7cfcec4cfcccfcfc4cfcccbc7"
              icon="bi bi-box-arrow-up-right"
            />
          </p>
          <h4>第7-1、7-2、85-1條修法提案說明</h4>
          <p class="txt">
            鄭委員正鈐：那全年度開的紅單總共有多少件？<br />
            王組長鳳輝：大概一千二百多萬件。<br />
            鄭委員正鈐：民眾檢舉開單占所有開單量的幾趴？<br />
            王組長鳳輝：<b>三分之一</b>。
          </p>
          <p class="txt">
            陳委員歐珀：..其實共同要面對的問題就是民眾檢舉的交通處罰要如何處理。本席在去年就提出這個修正草案，當時曾引發社會的熱論，大家也認為說這個確實是我們臺灣社會上所存在的一種很特殊的狀況。我們去瞭解之後發現，<b
              >世界上透過民眾檢舉作成處分的案子的國家也不多</b
            >...
          </p>
        </div>
        <div class="event">
          <p class="date">民國111年4月30日</p>
          <p class="txt">???</p>
        </div>
      </div>
      <hr />
      <h1>相關影片</h1>
      <div class="videobox">
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/OwPQwyNy7ek"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        />
      </div>
      <div class="videobox">
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/XLbjfJm19hY"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        />
      </div>
      <div class="videobox">
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/3pRnMH1iqrA"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        />
      </div>
      <hr />
      <h1>其他交通安全問題關鍵字</h1>
      <p>
        交通3E, 人行道, 路緣石, 禮讓行人, 停讓行人, 無障礙, 公車安全, 計程車,
        超時工作, 疲勞駕駛, A1A2A3, 路面邊線, 車道分向線, 工務局, 酒駕,
        十次車禍?次快, 標線型人行道, 防撞桿, 人行道增高, 速限, 自由車流,
        違規記點, 駕照改革, 小黃帽, 學習駕照, 善意違規, 人行道牽車,
        人行道機車格, 避車彎, 收費停車格, 交通基本法, 逼車, 區間測速,
        GRB政府資訊研究系統, 運輸研究所, 警政統計網, 開放資料, 兩段式左轉,
        偏心式左轉道, 圓環, 紅綠燈, 減速丘, 減速標線, 路霸, 盆栽, 騎樓稅金減免,
        機車駕訓補助, 交通安全教育, 執法, 工程, 交通工程技師, 隔熱紙透明度,
        安全車距, 安全超車距離, 自行車道
      </p>
      <hr />
      <div id="footer">
        by 交通平安熊安全
        <div>
          <IconButton
            title="Facebook"
            link="http://www.facebook.com/168bearsafety"
            icon="bi bi-facebook"
          />
          <IconButton
            title="Twitter"
            link="https://twitter.com/168bearsafety"
            icon="bi bi-twitter"
          />
          <IconButton
            title="YouTube"
            link="https://www.youtube.com/channel/UCw51lTf_nltYoUkZ1nGGoFw"
            icon="bi bi-youtube"
          />
          <IconButton
            title="GitHub"
            link="https://github.com/FOBshippingpoint/traffic-war-is-coming"
            icon="bi bi-github"
          />
        </div>
      </div>
    </section>
  </main>
</div>

<style>
  #bg {
    height: 100%;
    /* background-color: black; */
  }

  .date:first-child {
    padding-left: 5px;
  }

  main {
    font-family: "Noto Sans TC", sans-serif;
  }

  .unselectable {
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }

  .center {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  #title {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 64px;
    padding-top: 3em;
    padding-left: 0.5em;
    letter-spacing: 0.5em;
    margin: 0;
    margin-bottom: 0.5em;
    font-weight: bold;
    color: #f5f5f5;
    text-shadow: 2px 2px 6px black;
  }

  #countdown {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
  }

  #countdown > div {
    width: 2.5em;
    height: 2.5em;
    font-size: 64px;
    background: #cb1f1f;
    color: #e7ecef;
    box-shadow: 3px 3px 4px 0px rgba(0, 0, 0, 0.5);
    border-radius: 10%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  #countdown > div > span {
    font-size: 24px;
    position: absolute;
    margin-top: 5em;
    margin-left: 5em;
  }

  #photos {
    mask-image: linear-gradient(to top, rgba(0, 0, 0, 0), rgb(255, 255, 255));
    filter: brightness(0.5);
    height: 100%;
  }

  #photos-bg {
    position: absolute;
    z-index: -1;
    background: white;
    overflow: hidden;
  }

  #article {
    background-color: white;
    margin: 5% 25%;
    padding: 1em 2em;
    border-radius: 10px;
    box-shadow: 0px 0px 21px 7px rgba(0, 0, 0, 0.29);
  }

  @media screen and (max-width: 990px) {
    #article {
      margin: 5% 5%;
    }
  }

  /* @media screen and (max-width: 672px) {
    #countdown > div {
      font-size: 28px;
    }

    #countdown > div > span {
      font-size: 10.5px;
    }

    #title {
      font-size: 36px;
      letter-spacing: 0.5em;
    }

    #article {
      margin: 5% 0;
    }
  } */

  @media all and (min-width: 320px) and (max-width: 750px) {
    #countdown > div {
      font-size: 28px;
    }

    #countdown > div > span {
      font-size: 10.5px;
    }

    #title {
      font-size: 36px;
      letter-spacing: 0.5em;
    }

    #article {
      margin: 5% 0;
    }
  }

  @media all and (min-width: 751px) and (max-width: 1024px) {
    #countdown > div {
      font-size: 48px;
    }

    #countdown > div > span {
      font-size: 18px;
    }

    #title {
      font-size: 62px;
      letter-spacing: 0.5em;
    }

    #article {
      margin: 5% 10%;
    }
  }

  @media all and (min-width: 1025px) and (max-width: 1600px) {
    #countdown > div {
      font-size: 64px;
    }

    #countdown > div > span {
      font-size: 24px;
    }

    #title {
      font-size: 72px;
      letter-spacing: 0.5em;
    }

    #article {
      margin: 5% 20%;
    }
  }

  @media all and (min-width: 1601px) {
    #article {
      margin: 5% 30%;
    }
  }

  :global(body, html) {
    margin: 0;
    padding: 0;
  }

  #article > h1 {
    text-align: center;
  }

  #footer {
    text-align: center;
  }

  hr {
    background-color: #fff;
    padding: 0;
    margin: 30px;
    border: 0;
    height: 0;
    border-top: 1px solid #8c8c8c;
  }
</style>
