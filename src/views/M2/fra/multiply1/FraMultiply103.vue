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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply1-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>3.</h1></div>
                        <div class="chapter_title ltr"><h1>Rester en phase avec l’Esprit Saint</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="back">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</p>

<ul>
	<li>Exemple: <span class="popup-link" @click = "popUp('pop1')"> Psaumes 66:4</span>

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>Toute la terre se prosterne devant toi et chante en ton honneur; Elle chante ton nom. -Pause.</p>
	<!-- end bible --></div>
	&laquo; Toute la terre se prosterne devant toi et chante en ton honneur ; Elle chante ton nom. &raquo; Prenons une pause et louons le Seigneur avec un chant simple.</li>
</ul>

</div>

<ul>
</ul>

<h2>Soin</h2>

<p>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la Fid&eacute;lit&eacute;</h2>

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

<p>Exemple: Un jour une femme est all&eacute;e rendre visite &agrave; sa voisine. Au cours de leur discussion elle partagea l&rsquo;&eacute;vangile avec sa voisine et cette derni&egrave;re pla&ccedil;a sa foi en Christ. Mais alors la femme commen&ccedil;a &agrave; pleurer. &laquo; Mon mari vient de d&eacute;c&eacute;der il y a juste 2 semaines. Pourquoi ne m&rsquo;as-tu pas dit ceci plus t&ocirc;t? &raquo; vous voyez, nous ne savons jamais quel sera le dernier jour des gens. C&rsquo;est pourquoi nous devons partager l&rsquo;&eacute;vangile &agrave; toute occasion.</p>

</div>
</div>

<div class="up">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><h2>+ Contexte</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p>Lorsque nous pla&ccedil;ons notre foi en J&eacute;sus, l&rsquo;Esprit de Dieu commence par vivre en nous. Il s&rsquo;appelle le Saint-Esprit, l&rsquo;Esprit de v&eacute;rit&eacute; et notre Aide. Son minist&egrave;re dans nos vies est si important que nous prendrons du temps pour &eacute;tudier notre relation avec Lui.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez 1 Corinthiens 2:14-3:3 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire 1 Corinthiens 2:14-3:3</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">14&nbsp;</sup>Mais l&#39;homme animal ne re&ccedil;oit pas les choses de l&#39;Esprit de Dieu, car elles sont une folie pour lui, et il ne peut les conna&icirc;tre, parce que c&#39;est spirituellement qu&#39;on en juge.</p>

<p><sup class="versenum">15&nbsp;</sup>L&#39;homme spirituel, au contraire, juge de tout, et il n&#39;est lui-m&ecirc;me jug&eacute; par personne.</p>

<p><sup class="versenum">16&nbsp;</sup>Car Qui a connu la pens&eacute;e du Seigneur, Pour l&#39;instruire? Or nous, nous avons la pens&eacute;e de Christ.</p>

<p><sup class="versenum">3:1 </sup>Pour moi, fr&egrave;res, ce n&#39;est pas comme &agrave; des hommes spirituels que j&#39;ai pu vous parler, mais comme &agrave; des hommes charnels, comme &agrave; des enfants en Christ.</p>

<p><sup class="versenum">2&nbsp;</sup>Je vous ai donn&eacute; du lait, non de la nourriture solide, car vous ne pouviez pas la supporter; et vous ne le pouvez pas m&ecirc;me &agrave; pr&eacute;sent, parce que vous &ecirc;tes encore charnels.</p>

<p><sup class="versenum">3&nbsp;</sup>En effet, puisqu&#39;il y a parmi vous de la jalousie et des disputes, n&#39;&ecirc;tes-vous pas charnels, et ne marchez-vous pas selon l&#39;homme?</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<h2>Discussion de D&eacute;couverte</h2>

<ul>
	<li>Chacun dit ce qui a retenu son attention (ou ce qu&rsquo;il a aim&eacute; le plus) et pourquoi.</li>
	<li>Pourquoi pensez-vous que cette histoire est importante?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire (passage)?</li>
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

<ul>
	<li>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<ul>
	<li class="nobreak-final-final">Bien que l&rsquo;Esprit vit en tous les chr&eacute;tiens, ce n&rsquo;est pas tous les chr&eacute;tiens qui sont dirig&eacute;s et habilit&eacute;s par l&rsquo;Esprit. Quand nous nous fions &agrave; nos propres efforts ou dirigeons nos vies, la Bible nous appelle des charnels et nous n&rsquo;exp&eacute;rimentons pas une vie abondante ou fructueuse. Lisez <span class="popup-link" @click = "popUp('pop2')"> Galates 5:22-24</span>.

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">22&nbsp;</sup>Mais le fruit de l&#39;Esprit, c&#39;est l&#39;amour, la joie, la paix, la patience, la bont&eacute;, la b&eacute;nignit&eacute;, la fid&eacute;lit&eacute;, la douceur, la temp&eacute;rance;</p>

	<p><sup class="versenum">23&nbsp;</sup>la loi n&#39;est pas contre ces choses.</p>

	<p><sup class="versenum">24&nbsp;</sup>Ceux qui sont &agrave; J&eacute;sus Christ ont crucifi&eacute; la chair avec ses passions et ses d&eacute;sirs.</p>
	<!-- end bible --></div>
	Nous pouvons utiliser trois cercles pour nous aider &agrave; nous rappeler les trois types d&rsquo;hommes d&eacute;crits dans 1 Corinthiens (dessinez les trois cercles).</li>
</ul>

<p>Pour une &eacute;tude plus approfondie: Lisez le Message Transmissible #3: Comment &ecirc;tre rempli du Saint-Esprit et discuter avec un autre membre du groupe.</p>

</div>
</div>

<div class="forward">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary4" class="summary"><h2>+ Se Pr&eacute;parer pour la Mission</h2></div>
<div class="collapsed" id ="Text4">
<!-- end default revealSummary -->

<p>P&egrave;re, j&rsquo;ai besoin de toi. Je reconnais que j&#39;ai &eacute;t&eacute; le ma&icirc;tre de ma vie, et que j&#39;ai p&eacute;ch&eacute; contre Toi merci de m&rsquo;avoir pardonn&eacute; &agrave; travers la mort de Christ sur la croix. Je t&rsquo;invite &agrave; prendre contr&ocirc;le de ma vie et &agrave; me remplir de Ton Esprit Saint.</p>

<ul>
	<li>Enseignez le principe de la Respiration Spirituelle</li>
	<li>Expirer &ndash; <span class="popup-link" @click = "popUp('pop3')"> 1 Jean 1:9</span>
	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">9&nbsp;</sup>Si nous confessons nos p&eacute;ch&eacute;s, il est fid&egrave;le et juste pour nous les pardonner, et pour nous purifier de toute iniquit&eacute;.</p>
	<!-- end bible --></div>
	confessons nos p&eacute;ch&eacute;s, acceptons changer notre attitude ou nos actions</li>
	<li>Inspirer &ndash; laissons Christ diriger notre vie</li>
	<li>Amenez-les &agrave; prier pour &ecirc;tre dirig&eacute;s et habilit&eacute;s par le Saint-Esprit</li>
	<li>Apprenez &agrave; dessiner les trois cercles et &agrave; enseigner le principe de la Respiration Spirituelle</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Identifiez trois personnes &agrave; qui vous pouvez dire ce que vous avez appris au sujet du Saint-Esprit.</li>
	<li>Identifiez deux personnes &agrave; qui vous parlerez de l&rsquo;&eacute;vangile cette semaine</li>
	<li>Ecrivez des promesses &laquo; Je le ferai d&rsquo;ici quand &raquo; et dites les &agrave; votre groupe.</li>
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

<ul>
	<li>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples</li>
</ul>
</div>

<div class="for-enrichment">Pour en savoir davantage veuillez lire le <!-- begin linkInternal capacitor-->
<span id= "Return1" class="internal-link" @click="this.goToPageAndSetReturn('/M2/fra/tc/ct03', '#1')">
    Message transmissible N&deg; 3 : Rempli du Saint Esprit 
</span>
<!-- end linkInternal capacitor-->
 et en discuter avec un autre membre du groupe.</div>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Rester en phase avec l’Esprit Saint: ', '/content/M2/fra/multiply1/multiply103.html')">
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