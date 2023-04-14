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
                        <div class="chapter_number ltr"><h1>11.</h1></div>
                        <div class="chapter_title ltr"><h1>Etre un Témoin</h1></div>
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
	<li>Exemple: Lisez <span class="popup-link" @click = "popUp('pop1')"> Psaumes 95:1-7</span>&nbsp;et ex&eacute;cutez des chants.

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Venez, chantons avec all&eacute;gresse &agrave; l&#39;&Eacute;ternel! Poussons des cris de joie vers le rocher de notre salut.</p>

	<p><sup class="versenum">2&nbsp;</sup>Allons au-devant de lui avec des louanges, Faisons retentir des cantiques en son honneur!</p>

	<p><sup class="versenum">3&nbsp;</sup>Car l&#39;&Eacute;ternel est un grand Dieu, Il est un grand roi au-dessus de tous les dieux.</p>

	<p><sup class="versenum">4&nbsp;</sup>Il tient dans sa main les profondeurs de la terre, Et les sommets des montagnes sont &agrave; lui.</p>

	<p><sup class="versenum">5&nbsp;</sup>La mer est &agrave; lui, c&#39;est lui qui l&#39;a faite; La terre aussi, ses mains l&#39;ont form&eacute;e.</p>

	<p><sup class="versenum">6&nbsp;</sup>Venez, prosternons-nous et humilions-nous, Fl&eacute;chissons le genou devant l&#39;&Eacute;ternel, notre cr&eacute;ateur!</p>

	<p><sup class="versenum">7&nbsp;</sup>Car il est notre Dieu, Et nous sommes le peuple de son p&acirc;turage, Le troupeau que sa main conduit... Oh! si vous pouviez &eacute;couter aujourd&#39;hui sa voix!</p>
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

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

<ul>
	<li class="nobreak-final-final">Exemple: Dans le livre des Actes, nous voyons comment les croyants ont enseign&eacute; certains, et les ont faits formateurs des autres. Barnabas &eacute;tait l&rsquo;un des premiers disciples de J&eacute;sus. Il a trouv&eacute; un nouveau croyant du nom de Paul, et l&rsquo;aida. Celui-ci trouva Timoth&eacute;e et l&rsquo;aida aussi. Il prit Timoth&eacute;e avec lui pour annoncer l&rsquo;&eacute;vangile &agrave; plusieurs endroits. Plus tard, Paul envoya une lettre &agrave; Timoth&eacute;e dans laquelle il lui demandait d&rsquo;enseigner des hommes fid&egrave;les dans les &eacute;glises pour que ces derniers puissent &agrave; leur tour trouver et enseigner d&rsquo;autres jeunes chr&eacute;tiens. Lisez <span class="popup-link" @click = "popUp('pop2')"> 2 Timoth&eacute;e 2:2</span>.&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">2&nbsp;</sup>Et ce que tu as entendu de moi en pr&eacute;sence de beaucoup de t&eacute;moins, confie-le &agrave; des hommes fid&egrave;les, qui soient capables de l&#39;enseigner aussi &agrave; d&#39;autres.</p>
	<!-- end bible --></div>
	J&eacute;sus enseigna Barnabas, Barnabas enseigna Paul, Paul enseigna Timoth&eacute;e, Timoth&eacute;e enseigna des hommes fid&egrave;les qui &agrave; leur tour enseign&egrave;rent des jeunes. Tous les chr&eacute;tiens sont appel&eacute;s &agrave; enseigner des gens capables d&rsquo;en faire autant et ainsi de suite. De cette fa&ccedil;on, l&rsquo;&Eacute;vangile se r&eacute;pandra rapidement.</li>
</ul>

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

<p>Apr&egrave;s que J&eacute;sus fut ressuscit&eacute; d&rsquo;entre les morts, il continua &agrave; enseigner ses disciples &agrave; propos du Royaume de Dieu. Lors de sa derni&egrave;re rencontre avec eux, il mit un accent particulier sur la mission pour laquelle ils &eacute;taient appel&eacute;s ainsi que l&rsquo;aide qui leur sera apport&eacute;e dans la mission.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Actes 1:1-8 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 1:1-8</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Th&eacute;ophile, j&#39;ai parl&eacute;, dans mon premier livre, de tout ce que J&eacute;sus a commenc&eacute; de faire et d&#39;enseigner d&egrave;s le commencement</p>

<p><sup class="versenum">2&nbsp;</sup>jusqu&#39;au jour o&ugrave; il fut enlev&eacute; au ciel, apr&egrave;s avoir donn&eacute; ses ordres, par le Saint Esprit, aux ap&ocirc;tres qu&#39;il avait choisis.</p>

<p><sup class="versenum">3&nbsp;</sup>Apr&egrave;s qu&#39;il eut souffert, il leur apparut vivant, et leur en donna plusieurs preuves, se montrant &agrave; eux pendant quarante jours, et parlant des choses qui concernent le royaume de Dieu.</p>

<p><sup class="versenum">4&nbsp;</sup>Comme il se trouvait avec eux, il leur recommanda de ne pas s&#39;&eacute;loigner de J&eacute;rusalem, mais d&#39;attendre ce que le P&egrave;re avait promis, ce que je vous ai annonc&eacute;, leur dit-il;</p>

<p><sup class="versenum">5&nbsp;</sup>car Jean a baptis&eacute; d&#39;eau, mais vous, dans peu de jours, vous serez baptis&eacute;s du Saint Esprit.</p>

<p><sup class="versenum">6&nbsp;</sup>Alors les ap&ocirc;tres r&eacute;unis lui demand&egrave;rent: Seigneur, est-ce en ce temps que tu r&eacute;tabliras le royaume d&#39;Isra&euml;l?</p>

<p><sup class="versenum">7&nbsp;</sup>Il leur r&eacute;pondit: Ce n&#39;est pas &agrave; vous de conna&icirc;tre les temps ou les moments que le P&egrave;re a fix&eacute;s de sa propre autorit&eacute;.</p>

<p><sup class="versenum">8&nbsp;</sup>Mais vous recevrez une puissance, le Saint Esprit survenant sur vous, et vous serez mes t&eacute;moins &agrave; J&eacute;rusalem, dans toute la Jud&eacute;e, dans la Samarie, et jusqu&#39;aux extr&eacute;mit&eacute;s de la terre.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/111.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 1:1-8&nbsp; </button>
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

<p>Si nous d&eacute;cidons de suivre J&eacute;sus, nous d&eacute;cidons ainsi d&rsquo;ob&eacute;ir &agrave; Son commandement, celui d&rsquo;&ecirc;tre ses t&eacute;moins. Cependant, nous ne pouvons y arriver qu&rsquo;avec l&rsquo;aide de la puissance du Saint Esprit dans nos vies. Nous serons des t&eacute;moins efficaces seulement s&rsquo;Il nous fortifie. Le d&eacute;sir de Dieu est que nous t&eacute;moignions. Ce que Dieu voudrait est que nous t&eacute;moignions &agrave; tout le monde, ceux qui sont comme nous, et ceux qui ne le sont pas, ceux qui vivent dans notre entourage, et partout dans le monde.</p>

<p>Pour une &eacute;tude plus approfondie: Lisez le <!-- begin linkInternal capacitor-->
<span id= "Return1" class="internal-link" @click="this.goToPageAndSetReturn('/M2/fra/tc/ct05', '#1')">
    Message transmissible N&deg; 5  
</span>
<!-- end linkInternal capacitor-->
: Comment &ecirc;tre un t&eacute;moin fructueux, et discutez avec un autre membre du groupe.</p>

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
	<li>Rappelez-leur: Le succ&egrave;s dans le t&eacute;moignage vient de l&rsquo;initiative que nous prenons &agrave; partager Christ dans la puissance du Saint-Esprit, et &agrave; laisser les r&eacute;sultats &agrave; Dieu.</li>
	<li>R&eacute;visez le principe de la respiration spirituelle, et cr&eacute;ez une occasion personnelle pour expirer et inspirer</li>
	<li>Consacrez du temps &agrave; la pri&egrave;re pour &ecirc;tre dirig&eacute;s et habilit&eacute;s par l&rsquo;Esprit Saint.</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Identifiez 5 personnes de votre liste de r&eacute;seau, envers qui vous prendrez l&rsquo;initiative de faire le minist&egrave;re cette semaine.
	<ul>
		<li>Utilisez ce que vous avez appris cette semaine avec au moins trois de ces personnes.</li>
	</ul>
	</li>
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

<ul>
	<li>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</li>
</ul>
</div>

<div class="for-enrichment">Pour en savoir davantage veuillez lire le <!-- begin linkInternal capacitor-->
<span id= "Return2" class="internal-link" @click="this.goToPageAndSetReturn('/M2/fra/tc/ct05', '#2')">
    Message transmissible N&deg; 5 : T&eacute;moigner par l&#39;Esprit 
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

			<td class="social" @click="share('lesson', 'Etre un Témoin: ', '/content/M2/fra/multiply1/multiply111.html')">
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