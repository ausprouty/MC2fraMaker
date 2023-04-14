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
                        <div class="chapter_number ltr"><h1>10.</h1></div>
                        <div class="chapter_title ltr"><h1>Mon Histoire</h1></div>
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
	<li>Exemple: Lisez <span class="popup-link" @click = "popUp('pop1')"> Psaumes 66:1-4</span>&nbsp;et ex&eacute;cutez des chants.

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Au chef des chantres. Cantique. Psaume. Poussez vers Dieu des cris de joie, Vous tous, habitants de la terre!</p>

	<p><sup class="versenum">2&nbsp;</sup>Chantez la gloire de son nom, C&eacute;l&eacute;brez sa gloire par vos louanges!</p>

	<p><sup class="versenum">3&nbsp;</sup>Dites &agrave; Dieu: Que tes oeuvres sont redoutables! A cause de la grandeur de ta force, tes ennemis te flattent.</p>

	<p><sup class="versenum">4&nbsp;</sup>Toute la terre se prosterne devant toi et chante en ton honneur; Elle chante ton nom. -Pause.</p>
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

<p>Exemple: Dans <span class="popup-link" @click = "popUp('pop2')"> Jean 3: 8</span>.&nbsp;</p>

<div class="popup invisible" id="pop2"><!-- begin bible -->
<p><sup class="versenum">8&nbsp;</sup>Le vent souffle o&ugrave; il veut, et tu en entends le bruit; mais tu ne sais d&#39;o&ugrave; il vient, ni o&ugrave; il va. Il en est ainsi de tout homme qui est n&eacute; de l&#39;Esprit.</p>
<!-- end bible --></div>
l&#39;Esprit de Dieu est pr&eacute;sent&eacute; comme le vent. Nous ne pouvons ni le contr&ocirc;ler ni le faire bouger; Il souffle o&ugrave; Il veut. Nous ne pouvons pas cr&eacute;er de mouvements, seul l&#39;Esprit de Dieu peut le faire. Cependant, nous pouvons nous positionner de telle sorte que lorsqu&rsquo;il bouge, nous soyons pr&ecirc;ts &agrave; bouger avec Lui. Les simples comp&eacute;tences que vous apprenez aident &agrave; faire cela. La bonne nouvelle est la suivante: l&#39;Esprit de Dieu est &agrave; l&rsquo;&oelig;uvre partout! Continuons &agrave; nous pr&eacute;parer et &agrave; prier pour que l&#39;Esprit bouge.

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

<p>Paul avait &eacute;t&eacute; arr&ecirc;t&eacute; parce qu&#39;il avait &eacute;t&eacute; faussement accus&eacute; par les dirigeants juifs. Ils l&rsquo;accusent d&#39;avoir enfreint une loi du temple. Pendant sa d&eacute;fense devant le gouverneur, Paul a partag&eacute; l&#39;histoire de la fa&ccedil;on dont il a connu Christ.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ouobservez Actes 22:1-21 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 22:1-21</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Hommes fr&egrave;res et p&egrave;res, &eacute;coutez ce que j&#39;ai maintenant &agrave; vous dire pour ma d&eacute;fense!</p>

<p><sup class="versenum">2&nbsp;</sup>Lorsqu&#39;ils entendirent qu&#39;il leur parlait en langue h&eacute;bra&iuml;que, ils redoubl&egrave;rent de silence. Et Paul dit:</p>

<p><sup class="versenum">3&nbsp;</sup>je suis Juif, n&eacute; &agrave; Tarse en Cilicie; mais j&#39;ai &eacute;t&eacute; &eacute;lev&eacute; dans cette ville-ci, et instruit aux pieds de Gamaliel dans la connaissance exacte de la loi de nos p&egrave;res, &eacute;tant plein de z&egrave;le pour Dieu, comme vous l&#39;&ecirc;tes tous aujourd&#39;hui.</p>

<p><sup class="versenum">4&nbsp;</sup>J&#39;ai pers&eacute;cut&eacute; &agrave; mort cette doctrine, liant et mettant en prison hommes et femmes.</p>

<p><sup class="versenum">5&nbsp;</sup>Le souverain sacrificateur et tout le coll&egrave;ge des anciens m&#39;en sont t&eacute;moins. J&#39;ai m&ecirc;me re&ccedil;u d&#39;eux des lettres pour les fr&egrave;res de Damas, o&ugrave; je me rendis afin d&#39;amener li&eacute;s &agrave; J&eacute;rusalem ceux qui se trouvaient l&agrave; et de les faire punir.</p>

<p><sup class="versenum">6&nbsp;</sup>Comme j&#39;&eacute;tais en chemin, et que j&#39;approchais de Damas, tout &agrave; coup, vers midi, une grande lumi&egrave;re venant du ciel resplendit autour de moi.</p>

<p><sup class="versenum">7&nbsp;</sup>Je tombai par terre, et j&#39;entendis une voix qui me disait: Saul, Saul, pourquoi me pers&eacute;cutes-tu?</p>

<p><sup class="versenum">8&nbsp;</sup>Je r&eacute;pondis: Qui es-tu, Seigneur? Et il me dit: Je suis J&eacute;sus de Nazareth, que tu pers&eacute;cutes.</p>

<p><sup class="versenum">9&nbsp;</sup>Ceux qui &eacute;taient avec moi virent bien la lumi&egrave;re, mais ils n&#39;entendirent pas la voix de celui qui parlait. Alors je dis: Que ferai-je, Seigneur?</p>

<p><sup class="versenum">10&nbsp;</sup>Et le Seigneur me dit: L&egrave;ve-toi, va &agrave; Damas, et l&agrave; on te dira tout ce que tu dois faire.</p>

<p><sup class="versenum">11&nbsp;</sup>Comme je ne voyais rien, &agrave; cause de l&#39;&eacute;clat de cette lumi&egrave;re, ceux qui &eacute;taient avec moi me prirent par la main, et j&#39;arrivai &agrave; Damas.</p>

<p><sup class="versenum">12&nbsp;</sup>Or, un nomm&eacute; Ananias, homme pieux selon la loi, et de qui tous les Juifs demeurant &agrave; Damas rendaient un bon t&eacute;moignage, vint se pr&eacute;senter &agrave; moi,</p>

<p><sup class="versenum">13&nbsp;</sup>et me dit: Saul, mon fr&egrave;re, recouvre la vue. Au m&ecirc;me instant, je recouvrai la vue et je le regardai.</p>

<p><sup class="versenum">14&nbsp;</sup>Il dit: Le Dieu de nos p&egrave;res t&#39;a destin&eacute; &agrave; conna&icirc;tre sa volont&eacute;, &agrave; voir le Juste, et &agrave; entendre les paroles de sa bouche;</p>

<p><sup class="versenum">15&nbsp;</sup>car tu lui serviras de t&eacute;moin, aupr&egrave;s de tous les hommes, des choses que tu as vues et entendues.</p>

<p><sup class="versenum">16&nbsp;</sup>Et maintenant, que tardes-tu? L&egrave;ve-toi, sois baptis&eacute;, et lav&eacute; de tes p&eacute;ch&eacute;s, en invoquant le nom du Seigneur.</p>

<p><sup class="versenum">17&nbsp;</sup>De retour &agrave; J&eacute;rusalem, comme je priais dans le temple, je fus ravi en extase,</p>

<p><sup class="versenum">18&nbsp;</sup>et je vis le Seigneur qui me disait: H&acirc;te-toi, et sors promptement de J&eacute;rusalem, parce qu&#39;ils ne recevront pas ton t&eacute;moignage sur moi.</p>

<p><sup class="versenum">19&nbsp;</sup>Et je dis: Seigneur, ils savent eux-m&ecirc;mes que je faisais mettre en prison et battre de verges dans les synagogues ceux qui croyaient en toi, et que,</p>

<p><sup class="versenum">20&nbsp;</sup>lorsqu&#39;on r&eacute;pandit le sang d&#39;&Eacute;tienne, ton t&eacute;moin, j&#39;&eacute;tais moi-m&ecirc;me pr&eacute;sent, joignant mon approbation &agrave; celle des autres, et gardant les v&ecirc;tements de ceux qui le faisaient mourir.</p>

<p><sup class="versenum">21&nbsp;</sup>Alors il me dit: Va, je t&#39;enverrai au loin vers les nations...</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/110.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 22:1-21&nbsp; </button>
    <div class="collapsed"></div>

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
	<li>Relisez l&rsquo;histoire. D&eacute;signez quelqu&rsquo;un pour raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<p>L&rsquo;histoire (t&eacute;moignage) de Paul peut &ecirc;tre r&eacute;sum&eacute;e en trois points:</p>

<ul>
	<li>Sa vie d&rsquo;avant Christ,</li>
	<li>comment il a rencontr&eacute; Christ, et</li>
	<li>sa vie apr&egrave;s qu&rsquo;il ait rencontr&eacute; Christ.</li>
</ul>

<p>Ce mod&egrave;le est toujours un moyen efficace de dire aux autres ce que J&eacute;sus a fait dans nos vies. Nos histoires sont un t&eacute;moignage puissant des bienfaits de la connaissance du Seigneur.</p>

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

<ul>
	<li>Donnez un exemple r&eacute;cent en racontant votre propre histoire et en soulignant les 3 parties</li>
	<li>Exercez-vous &agrave; partager vos histoires les uns avec les autres.</li>
	<li>Demandez-leur de choisir 1 mot qui d&eacute;crit les 3 parties de leur histoire</li>
	<li>Demandez-leur de l&#39;agrandir en &eacute;crivant 2-3 phrases pour chacune des 3 parties.</li>
	<li>Demandez-leur de raconter leur histoire avec un partenaire. Apr&egrave;s 3 minutes, demandez-leur de donner leur avis, puis arr&ecirc;tez.</li>
	<li>Si le temps le permet, demandez-leur de changer de partenaire, et de reprendre le m&ecirc;me processus.</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<p>o Utilisez ce que vous avez appris cette semaine avec au moins trois de ces personnes.</p>

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
</div>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Mon Histoire: ', '/content/M2/fra/multiply1/multiply110.html')">
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