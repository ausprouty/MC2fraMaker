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
                        <div class="chapter_number ltr"><h1>13.</h1></div>
                        <div class="chapter_title ltr"><h1>S’engager les uns pour les autres</h1></div>
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

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration</p>

<ul>
	<li>Exemple: Lisez <span class="popup-link" @click = "popUp('pop1')"> Psaumes 100</span>&nbsp;&nbsp;et ex&eacute;cutez des chants.

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><sup class="versenum">1 </sup>Psaume de louange. Poussez vers l&#39;&Eacute;ternel des cris de joie, Vous tous, habitants de la terre!</p>

	<p><sup class="versenum">2&nbsp;</sup>Servez l&#39;&Eacute;ternel, avec joie, Venez avec all&eacute;gresse en sa pr&eacute;sence!</p>

	<p><sup class="versenum">3&nbsp;</sup>Sachez que l&#39;&Eacute;ternel est Dieu! C&#39;est lui qui nous a faits, et nous lui appartenons; Nous sommes son peuple, et le troupeau de son p&acirc;turage.</p>

	<p><sup class="versenum">4&nbsp;</sup>Entrez dans ses portes avec des louanges, Dans ses parvis avec des cantiques! C&eacute;l&eacute;brez-le, b&eacute;nissez son nom!</p>

	<p><sup class="versenum">5&nbsp;</sup>Car l&#39;&Eacute;ternel est bon; sa bont&eacute; dure toujours, Et sa fid&eacute;lit&eacute; de g&eacute;n&eacute;ration en g&eacute;n&eacute;ration.</p>
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<!-- end bible --></div>
	</li>
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

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

<p>Exemple: Lisez <span class="popup-link" @click = "popUp('pop2')"> Ephesiens 2:1-10</span>.&nbsp;</p>

<div class="popup invisible" id="pop2"><!-- begin bible -->
<p><sup class="versenum">1 </sup>Vous &eacute;tiez morts par vos offenses et par vos p&eacute;ch&eacute;s,</p>

<p><sup class="versenum">2&nbsp;</sup>dans lesquels vous marchiez autrefois, selon le train de ce monde, selon le prince de la puissance de l&#39;air, de l&#39;esprit qui agit maintenant dans les fils de la r&eacute;bellion.</p>

<p><sup class="versenum">3&nbsp;</sup>Nous tous aussi, nous &eacute;tions de leur nombre, et nous vivions autrefois selon les convoitises de notre chair, accomplissant les volont&eacute;s de la chair et de nos pens&eacute;es, et nous &eacute;tions par nature des enfants de col&egrave;re, comme les autres...</p>

<p><sup class="versenum">4&nbsp;</sup>Mais Dieu, qui est riche en mis&eacute;ricorde, &agrave; cause du grand amour dont il nous a aim&eacute;s,</p>

<p><sup class="versenum">5&nbsp;</sup>nous qui &eacute;tions morts par nos offenses, nous a rendus &agrave; la vie avec Christ (c&#39;est par gr&acirc;ce que vous &ecirc;tes sauv&eacute;s);</p>

<p><sup class="versenum">6&nbsp;</sup>il nous a ressuscit&eacute;s ensemble, et nous a fait asseoir ensemble dans les lieux c&eacute;lestes, en J&eacute;sus Christ,</p>

<p><sup class="versenum">7&nbsp;</sup>afin de montrer dans les si&egrave;cles &agrave; venir l&#39;infinie richesse de sa gr&acirc;ce par sa bont&eacute; envers nous en J&eacute;sus Christ.</p>

<p><sup class="versenum">8&nbsp;</sup>Car c&#39;est par la gr&acirc;ce que vous &ecirc;tes sauv&eacute;s, par le moyen de la foi. Et cela ne vient pas de vous, c&#39;est le don de Dieu.</p>

<p><sup class="versenum">9&nbsp;</sup>Ce n&#39;est point par les oeuvres, afin que personne ne se glorifie.</p>

<p><sup class="versenum">10&nbsp;</sup>Car nous sommes son ouvrage, ayant &eacute;t&eacute; cr&eacute;&eacute;s en J&eacute;sus Christ pour de bonnes oeuvres, que Dieu a pr&eacute;par&eacute;es d&#39;avance, afin que nous les pratiquions.</p>
<!-- end bible --></div>
N&rsquo;est-ce pas merveilleux? Nous &eacute;tions morts dans nos p&eacute;ch&eacute;s, mais Dieu nous a rendus vivants. Il a fait tout ceci afin que vous puissiez accomplir les bonnes &oelig;uvres qu&rsquo;Il a pr&eacute;par&eacute;es pour vous. Nos vies sont pleines d&rsquo;objectifs et de sens! Encourageons-nous mutuellement en nous rappelant ces v&eacute;rit&eacute;s.

<p>&nbsp;</p>

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

<p>Au cours d&rsquo;une f&ecirc;te juive appel&eacute;e Pentec&ocirc;te, les Juifs de partout dans le monde &eacute;taient &agrave; J&eacute;rusalem. Dieu envoya le Saint Esprit sur 120 de ses fid&egrave;les qui se sont rassembl&eacute;s. Par la puissance de l&rsquo;Esprit, les 120 fid&egrave;les commenc&egrave;rent &agrave; parler dans les langues des visiteurs qui venaient de partout dans le monde. Pierre se mit &agrave; pr&ecirc;cher &agrave; une foule au sujet de la mort et de la r&eacute;surrection de J&eacute;sus, prouvant qu&rsquo;Il &eacute;tait le Messie. Comme r&eacute;sultat, 3000 personnes crurent et furent baptis&eacute;es. Mais qu&rsquo;est-ce qui est arriv&eacute; apr&egrave;s qu&rsquo;ils ont cru.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Actes 2:41-47 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 2:41-47</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">41&nbsp;</sup>Ceux qui accept&egrave;rent sa parole furent baptis&eacute;s; et, en ce jour-l&agrave;, le nombre des disciples s&#39;augmenta d&#39;environ trois mille &acirc;mes.</p>

<p><sup class="versenum">42&nbsp;</sup>Ils pers&eacute;v&eacute;raient dans l&#39;enseignement des ap&ocirc;tres, dans la communion fraternelle, dans la fraction du pain, et dans les pri&egrave;res.</p>

<p><sup class="versenum">43&nbsp;</sup>La crainte s&#39;emparait de chacun, et il se faisait beaucoup de prodiges et de miracles par les ap&ocirc;tres.</p>

<p><sup class="versenum">44&nbsp;</sup>Tous ceux qui croyaient &eacute;taient dans le m&ecirc;me lieu, et ils avaient tout en commun.</p>

<p><sup class="versenum">45&nbsp;</sup>Ils vendaient leurs propri&eacute;t&eacute;s et leurs biens, et ils en partageaient le produit entre tous, selon les besoins de chacun.</p>

<p><sup class="versenum">46&nbsp;</sup>Ils &eacute;taient chaque jour tous ensemble assidus au temple, ils rompaient le pain dans les maisons, et prenaient leur nourriture avec joie et simplicit&eacute; de coeur,</p>

<p><sup class="versenum">47&nbsp;</sup>louant Dieu, et trouvant gr&acirc;ce aupr&egrave;s de tout le peuple. Et le Seigneur ajoutait chaque jour &agrave; l&#39;&Eacute;glise ceux qui &eacute;taient sauv&eacute;s.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/113.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 2:41-47&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<ul>
	<li>Chacun dit ce qui a retenu son attention (ou ce qu&rsquo;il a aim&eacute; le plus) et pourquoi.</li>
	<li>Pourquoi pensez-vous que cette histoire est importante?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire (ce passage)?</li>
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
	<li>Relisez l&rsquo;histoire. Amenez quelqu&rsquo;un &agrave; raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<p>Lisez <span class="popup-link" @click = "popUp('pop3')"> Matthieu 16:18</span>.&nbsp;</p>

<div class="popup invisible" id="pop3"><!-- begin bible -->
<p><sup class="versenum">18&nbsp;</sup>Et moi, je te dis que tu es Pierre, et que sur cette pierre je b&acirc;tirai mon &Eacute;glise, et que les portes du s&eacute;jour des morts ne pr&eacute;vaudront point contre elle.</p>
<!-- end bible --></div>
Le Saint Esprit a conduit les premiers croyants &agrave; se rencontrer r&eacute;guli&egrave;rement pour l&rsquo;adoration, la pri&egrave;re, la communion fraternelle, l&rsquo;&eacute;tude de la Parole de Dieu, s&rsquo;aimant les uns les autres et pr&ecirc;chant &agrave; ceux qui ne connaissaient pas encore Christ. En chaque lieu mentionn&eacute; dans le livre des Actes, les gens &eacute;taient devenus des fid&egrave;les de Christ et ils ont pris le m&ecirc;me engagement les uns envers les autres. C&rsquo;est l&agrave; la description de l&rsquo;&eacute;glise locale!

<p>&nbsp;</p>

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

<p>Exercez-vous &agrave; reproduire le cercle de la sant&eacute; de l&rsquo;&eacute;glise comme un moyen facile pour vous rappeler de toutes les caract&eacute;ristiques de l&rsquo;&eacute;glise. Ceci inclut: l&rsquo;adoration, la communion fraternelle, l&rsquo;&eacute;tude de la Parole de Dieu, la Sainte C&egrave;ne, le bapt&ecirc;me, le minist&egrave;re, le t&eacute;moignage, des leaders qui donnent et prendre soin.</p>

<p>&laquo; Ce groupe veut-il prendre cet engagement les uns envers les autres? Pour &ecirc;tre l&rsquo;Eglise du Seigneur en ce lieu? &raquo;.</p>

<ul>
	<li>Discutez de ce qui suit:</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<p>Identifiez 5 personnes de votre Liste de R&eacute;seau envers qui vous prendrez l&rsquo;initiative de faire le minist&egrave;re cette semaine.</p>

<p>Ecrivez les promesses &laquo; Je le ferai d&rsquo;ici quand&raquo;.</p>

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

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser pour initier un mouvement de faiseurs de disciples.</p>
</div>

<div class="for-enrichment">Pour en savoir davantage veuillez lire le <!-- begin linkInternal capacitor-->
<span id= "Return1" class="internal-link" @click="this.goToPageAndSetReturn('/M2/fra/tc/ct08', '#1')">
    Message transmissible N&deg; 8 : Comment Aimer par la Foi 
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

			<td class="social" @click="share('lesson', 'S’engager les uns pour les autres: ', '/content/M2/fra/multiply1/multiply113.html')">
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