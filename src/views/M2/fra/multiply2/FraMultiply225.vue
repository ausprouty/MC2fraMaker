<script>
import SQLiteService from '@/services/SQLiteService.js'
import { useFindSummaries, useFindCollapsible, usePopUp} from "@/assets/javascript/revealText.js"
import { useRevealMedia } from "@/assets/javascript/revealMedia.js"
import { useShare} from "@/assets/javascript/share.js"


export default {
   methods:{
    async addNote(noteid){
       var noteText = document.getElementById(noteid).value
       var noteHeight = await SQLiteService.addNote(noteid, this.$route.name, noteText)
       document.getElementById(noteid).style.height = noteHeight
    },
    goToPageAndSetReturn(gotoPath){
      localStorage.setItem("returnpage", this.$route.name);
      this.$router.push({
        path: gotoPath,
      })
    },
    pageGoBack(returnto){
      if (localStorage.getItem("returnpage")) {
        returnto = localStorage.getItem("returnpage");
        localStorage.removeItem("returnpage")
      }
      this.$router.push({
        name: returnto,
      })
    },
    popUp(verse){
      usePopUp(verse)
    },
    share(what, v1, v2){
      useShare(what, v1, v2)
    },
    vuePush(id){
      this.$router.push({
        name: id,
      })
    },
  },
  async mounted() {
    localStorage.setItem("lastpage", this.$route.name)
    useFindSummaries()
    useFindCollapsible()
    useRevealMedia()
    await SQLiteService.notes(this.$route.name)
  },
}
</script>
<template>
  <div id="nav">
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply2-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>25.</h1></div>
                        <div class="chapter_title ltr"><h1>Jésus, quelqu’un qui dit la verité</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</p>

</div>

<h2>Soin</h2>

<p>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la Fid&eacute;lit&eacute;</h2>

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Jean 5:16-47 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 5:16-47</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">16&nbsp;</sup>C&#39;est pourquoi les Juifs poursuivaient J&eacute;sus, parce qu&#39;il faisait ces choses le jour du sabbat.</p>

<p><sup class="versenum">17&nbsp;</sup>Mais J&eacute;sus leur r&eacute;pondit: Mon P&egrave;re agit jusqu&#39;&agrave; pr&eacute;sent; moi aussi, j&#39;agis.</p>

<p><sup class="versenum">18&nbsp;</sup>A cause de cela, les Juifs cherchaient encore plus &agrave; le faire mourir, non seulement parce qu&#39;il violait le sabbat, mais parce qu&#39;il appelait Dieu son propre P&egrave;re, se faisant lui-m&ecirc;me &eacute;gal &agrave; Dieu.</p>

<p><sup class="versenum">19&nbsp;</sup>J&eacute;sus reprit donc la parole, et leur dit: En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, le Fils ne peut rien faire de lui-m&ecirc;me, il ne fait que ce qu&#39;il voit faire au P&egrave;re; et tout ce que le P&egrave;re fait, le Fils aussi le fait pareillement.</p>

<p><sup class="versenum">20&nbsp;</sup>Car le P&egrave;re aime le Fils, et lui montre tout ce qu&#39;il fait; et il lui montrera des oeuvres plus grandes que celles-ci, afin que vous soyez dans l&#39;&eacute;tonnement.</p>

<p><sup class="versenum">21&nbsp;</sup>Car, comme le P&egrave;re ressuscite les morts et donne la vie, ainsi le Fils donne la vie &agrave; qui il veut.</p>

<p><sup class="versenum">22&nbsp;</sup>Le P&egrave;re ne juge personne, mais il a remis tout jugement au Fils,</p>

<p><sup class="versenum">23&nbsp;</sup>afin que tous honorent le Fils comme ils honorent le P&egrave;re. Celui qui n&#39;honore pas le Fils n&#39;honore pas le P&egrave;re qui l&#39;a envoy&eacute;.</p>

<p><sup class="versenum">24&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, celui qui &eacute;coute ma parole, et qui croit &agrave; celui qui m&#39;a envoy&eacute;, a la vie &eacute;ternelle et ne vient point en jugement, mais il est pass&eacute; de la mort &agrave; la vie.</p>

<p><sup class="versenum">25&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, l&#39;heure vient, et elle est d&eacute;j&agrave; venue, o&ugrave; les morts entendront la voix du Fils de Dieu; et ceux qui l&#39;auront entendue vivront.</p>

<p><sup class="versenum">26&nbsp;</sup>Car, comme le P&egrave;re a la vie en lui-m&ecirc;me, ainsi il a donn&eacute; au Fils d&#39;avoir la vie en lui-m&ecirc;me.</p>

<p><sup class="versenum">27&nbsp;</sup>Et il lui a donn&eacute; le pouvoir de juger, parce qu&#39;il est Fils de l&#39;homme.</p>

<p><sup class="versenum">28&nbsp;</sup>Ne vous &eacute;tonnez pas de cela; car l&#39;heure vient o&ugrave; tous ceux qui sont dans les s&eacute;pulcres entendront sa voix, et en sortiront.</p>

<p><sup class="versenum">29&nbsp;</sup>Ceux qui auront fait le bien ressusciteront pour la vie, mais ceux qui auront fait le mal ressusciteront pour le jugement.</p>

<p><sup class="versenum">30&nbsp;</sup>Je ne puis rien faire de moi-m&ecirc;me: selon que j&#39;entends, je juge; et mon jugement est juste, parce que je ne cherche pas ma volont&eacute;, mais la volont&eacute; de celui qui m&#39;a envoy&eacute;.</p>

<p><sup class="versenum">31&nbsp;</sup>Si c&#39;est moi qui rends t&eacute;moignage de moi-m&ecirc;me, mon t&eacute;moignage n&#39;est pas vrai.</p>

<p><sup class="versenum">32&nbsp;</sup>Il y en a un autre qui rend t&eacute;moignage de moi, et je sais que le t&eacute;moignage qu&#39;il rend de moi est vrai.</p>

<p><sup class="versenum">33&nbsp;</sup>Vous avez envoy&eacute; vers Jean, et il a rendu t&eacute;moignage &agrave; la v&eacute;rit&eacute;.</p>

<p><sup class="versenum">34&nbsp;</sup>Pour moi ce n&#39;est pas d&#39;un homme que je re&ccedil;ois le t&eacute;moignage; mais je dis ceci, afin que vous soyez sauv&eacute;s.</p>

<p><sup class="versenum">35&nbsp;</sup>Jean &eacute;tait la lampe qui br&ucirc;le et qui luit, et vous avez voulu vous r&eacute;jouir une heure &agrave; sa lumi&egrave;re.</p>

<p><sup class="versenum">36&nbsp;</sup>Moi, j&#39;ai un t&eacute;moignage plus grand que celui de Jean; car les oeuvres que le P&egrave;re m&#39;a donn&eacute; d&#39;accomplir, ces oeuvres m&ecirc;mes que je fais, t&eacute;moignent de moi que c&#39;est le P&egrave;re qui m&#39;a envoy&eacute;.</p>

<p><sup class="versenum">37&nbsp;</sup>Et le P&egrave;re qui m&#39;a envoy&eacute; a rendu lui-m&ecirc;me t&eacute;moignage de moi. Vous n&#39;avez jamais entendu sa voix, vous n&#39;avez point vu sa face,</p>

<p><sup class="versenum">38&nbsp;</sup>et sa parole ne demeure point en vous, parce que vous ne croyez pas &agrave; celui qu&#39;il a envoy&eacute;.</p>

<p><sup class="versenum">39&nbsp;</sup>Vous sondez les &Eacute;critures, parce que vous pensez avoir en elles la vie &eacute;ternelle: ce sont elles qui rendent t&eacute;moignage de moi.</p>

<p><sup class="versenum">40&nbsp;</sup>Et vous ne voulez pas venir &agrave; moi pour avoir la vie!</p>

<p><sup class="versenum">41&nbsp;</sup>Je ne tire pas ma gloire des hommes.</p>

<p><sup class="versenum">42&nbsp;</sup>Mais je sais que vous n&#39;avez point en vous l&#39;amour de Dieu.</p>

<p><sup class="versenum">43&nbsp;</sup>Je suis venu au nom de mon P&egrave;re, et vous ne me recevez pas; si un autre vient en son propre nom, vous le recevrez.</p>

<p><sup class="versenum">44&nbsp;</sup>Comment pouvez-vous croire, vous qui tirez votre gloire les uns des autres, et qui ne cherchez point la gloire qui vient de Dieu seul?</p>

<p><sup class="versenum">45&nbsp;</sup>Ne pensez pas que moi je vous accuserai devant le P&egrave;re; celui qui vous accuse, c&#39;est Mo&iuml;se, en qui vous avez mis votre esp&eacute;rance.</p>

<p><sup class="versenum">46&nbsp;</sup>Car si vous croyiez Mo&iuml;se, vous me croiriez aussi, parce qu&#39;il a &eacute;crit de moi.</p>

<p><sup class="versenum">47&nbsp;</sup>Mais si vous ne croyez pas &agrave; ses &eacute;crits, comment croirez-vous &agrave; mes paroles?</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/225.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 5:16-47&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<p>Etudiez chaque passage en utilisant les questions de discussion suivantes:</p>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ?</li>
	<li>Qu&rsquo;est ce qui est nouveau ou s&rsquo;est d&eacute;velopp&eacute; &agrave; ce point de l&rsquo;histoire de J&eacute;sus?</li>
	<li>Quelle implication du point de vue de l&rsquo;humanit&eacute; ou de la divinit&eacute; de J&eacute;sus voyez-vous dans ce passage ?</li>
</ul>

<p>Questions suppl&eacute;mentaires que vous pouvez poser:</p>

<ul>
	<li>Qu&rsquo;est-ce que ses disciples apprennent?</li>
	<li>Qu&rsquo;est-ce que J&eacute;sus est en train de nous montrer au sujet de sa vie et de son minist&egrave;re (ou leadership) ?</li>
	<li>Qu&rsquo;est ce que J&eacute;sus est en train de montrer au sujet du leadership empreint de pi&eacute;t&eacute; ?</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note1Text')"
        id="note1Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Lire, raconter et corriger</h2>

<p>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</p>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p>J&eacute;sus d&eacute;clarait que Dieu est Son vrai P&egrave;re et que Lui et Dieu sont &eacute;gaux. J&eacute;sus se r&eacute;f&egrave;re &agrave; cinq t&eacute;moins pour soutenir Sa d&eacute;claration:</p>

<ol>
	<li>La d&eacute;claration de J&eacute;sus m&ecirc;me (v19-31).</li>
	<li>Le t&eacute;moignage de Jean-Baptiste (v33-35).</li>
	<li>Les &oelig;uvres de J&eacute;sus (v36).</li>
	<li>La voix du P&egrave;re (v37-38) &agrave; Son bapt&ecirc;me.</li>
	<li>L&rsquo;Ancien Testament (v39-47).</li>
</ol>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ Se Pr&eacute;parer pour la Mission</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<p><span class="tlid-translation translation" lang="fr"><span title="">Pratiquez les comp&eacute;tences n&eacute;cessaires ou les sujets pr&eacute;c&eacute;dents pour vous pr&eacute;parer &agrave; servir les autres:</span></span></p>

<ul>
	<li><span class="tlid-translation translation" lang="fr"><span title="">Pri&egrave;re, soins, partage</span></span></li>
	<li><span class="tlid-translation translation" lang="fr"><span title="">Gospel</span></span></li>
	<li><span class="tlid-translation translation" lang="fr"><span title="">&Eacute;tudes bibliques fondamentales.</span></span></li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission</h2>

<ul>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau envers qui vous prendrez l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>&Eacute;crivez les promesses &laquo; je le ferai d&rsquo;ici quand &raquo; et parlez-en &agrave; votre groupe.</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note2Text')"
        id="note2Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Prier pour la Mission</h2>

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</p>

<p>&nbsp;</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Jésus, quelqu’un qui dit la verité: ', '/content/M2/fra/multiply2/multiply225.html')">
				<img class="social" src="@/assets/sites/mc2/images/standard/Share.png" />
			</td>
		</tr>
	</tbody>
</table>
<div class="footer">
<p class="footer">MC2</p>
<p class="footer" @click="share('website', 'https://GlobalChurchMovements.org', '')"> GlobalChurchMovements.org</p>
</div>

<!-- end mc2 sdcard languageFooter -->
<!-- end sdcard languageFooterSingle -->

</div><!--- Created by publishPage-->

</template>
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->