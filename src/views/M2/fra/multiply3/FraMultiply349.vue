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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply3-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>49.</h1></div>
                        <div class="chapter_title ltr"><h1>Paul présente sa défense devant le nouveau gouverneur romain Festus</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p><em>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</em></p>

<ul>
	<li class="nobreak-final-final">(Facultatif) J&eacute;sus-Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re ; qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;. Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus-Christ homme, qui s&rsquo;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. (<span class="popup-link" @click = "popUp('pop1')"> Philippiens 2:11</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">11&nbsp;</sup>et que toute langue confesse que J&eacute;sus Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> 1 Timoth&eacute;e 2:4-6</span>)

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;.</p>

	<p><sup class="versenum">5&nbsp;</sup>Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus Christ homme,</p>

	<p><sup class="versenum">6&nbsp;</sup>qui s&#39;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. C&#39;est l&agrave; le t&eacute;moignage rendu en son propre temps,</p>
	<!-- end bible --></div>
	</li>
</ul>

</div>

<h2>Soin</h2>

<p><em>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</em></p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la fid&eacute;lit&eacute;</h2>

<p><em>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</em></p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Motivation et encouragement</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p><em>Trouvez un moyen de projeter une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux:</em></p>

<ul>
	<li class="indent">un passage qui leur rappelle le c&oelig;ur du P&egrave;re et de la vision final.</li>
	<li>r&eacute;fl&eacute;chir sur des changements intervenus dans leur vie depuis qu&rsquo;ils ont commenc&eacute; &agrave; suivre Christ</li>
	<li>leur rappeler ce que Dieu veut faire &agrave; travers eux</li>
</ul>

<p><strong>Partagez la GRANDE vision</strong> <em>&laquo; une &eacute;glise pour chaque village et communaut&eacute;, l&rsquo;&eacute;vangile pour chaque personne &raquo;.</em></p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><p>+ Contexte</p></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<ul>
	<li>Demandez au groupe de raconter l&rsquo;histoire de la semaine pass&eacute;e.</li>
</ul>

</div>

<h2>Lisez</h2>

<ul>
	<li>Lisez ou observez Actes 25:1-22 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 25:1-22</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Festus, &eacute;tant arriv&eacute; dans la province, monta trois jours apr&egrave;s de C&eacute;sar&eacute;e &agrave; J&eacute;rusalem.</p>

<p><sup class="versenum">2&nbsp;</sup>Les principaux sacrificateurs et les principaux d&#39;entre les Juifs lui port&egrave;rent plainte contre Paul. Ils firent des instances aupr&egrave;s de lui, et, dans des vues hostiles,</p>

<p><sup class="versenum">3&nbsp;</sup>lui demand&egrave;rent comme une faveur qu&#39;il le f&icirc;t venir &agrave; J&eacute;rusalem. Ils pr&eacute;paraient un guet-apens, pour le tuer en chemin.</p>

<p><sup class="versenum">4&nbsp;</sup>Festus r&eacute;pondit que Paul &eacute;tait gard&eacute; &agrave; C&eacute;sar&eacute;e, et que lui-m&ecirc;me devait partir sous peu.</p>

<p><sup class="versenum">5&nbsp;</sup>Que les principaux d&#39;entre vous descendent avec moi, dit-il, et s&#39;il y a quelque chose de coupable en cet homme, qu&#39;ils l&#39;accusent.</p>

<p><sup class="versenum">6&nbsp;</sup>Festus ne passa que huit &agrave; dix jours parmi eux, puis il descendit &agrave; C&eacute;sar&eacute;e. Le lendemain, s&#39;&eacute;tant assis sur son tribunal, il donna l&#39;ordre qu&#39;on amen&acirc;t Paul.</p>

<p><sup class="versenum">7&nbsp;</sup>Quand il fut arriv&eacute;, les Juifs qui &eacute;taient venus de J&eacute;rusalem l&#39;entour&egrave;rent, et port&egrave;rent contre lui de nombreuses et graves accusations, qu&#39;ils n&#39;&eacute;taient pas en &eacute;tat de prouver.</p>

<p><sup class="versenum">8&nbsp;</sup>Paul entreprit sa d&eacute;fense, en disant: Je n&#39;ai rien fait de coupable, ni contre la loi des Juifs, ni contre le temple, ni contre C&eacute;sar.</p>

<p><sup class="versenum">9&nbsp;</sup>Festus, d&eacute;sirant plaire aux Juifs, r&eacute;pondit &agrave; Paul: Veux-tu monter &agrave; J&eacute;rusalem, et y &ecirc;tre jug&eacute; sur ces choses en ma pr&eacute;sence?</p>

<p><sup class="versenum">10&nbsp;</sup>Paul dit: C&#39;est devant le tribunal de C&eacute;sar que je comparais, c&#39;est l&agrave; que je dois &ecirc;tre jug&eacute;. Je n&#39;ai fait aucun tort aux Juifs, comme tu le sais fort bien.</p>

<p><sup class="versenum">11&nbsp;</sup>Si j&#39;ai commis quelque injustice, ou quelque crime digne de mort, je ne refuse pas de mourir; mais, si les choses dont ils m&#39;accusent sont fausses, personne n&#39;a le droit de me livrer &agrave; eux. J&#39;en appelle &agrave; C&eacute;sar.</p>

<p><sup class="versenum">12&nbsp;</sup>Alors Festus, apr&egrave;s avoir d&eacute;lib&eacute;r&eacute; avec le conseil, r&eacute;pondit: Tu en as appel&eacute; &agrave; C&eacute;sar; tu iras devant C&eacute;sar.</p>

<p><sup class="versenum">13&nbsp;</sup>Quelques jours apr&egrave;s, le roi Agrippa et B&eacute;r&eacute;nice arriv&egrave;rent &agrave; C&eacute;sar&eacute;e, pour saluer Festus.</p>

<p><sup class="versenum">14&nbsp;</sup>Comme ils pass&egrave;rent l&agrave; plusieurs jours, Festus exposa au roi l&#39;affaire de Paul, et dit: F&eacute;lix a laiss&eacute; prisonnier un homme</p>

<p><sup class="versenum">15&nbsp;</sup>contre lequel, lorsque j&#39;&eacute;tais &agrave; J&eacute;rusalem, les principaux sacrificateurs et les anciens des Juifs ont port&eacute; plainte, en demandant sa condamnation.</p>

<p><sup class="versenum">16&nbsp;</sup>Je leur ai r&eacute;pondu que ce n&#39;est pas la coutume des Romains de livrer un homme avant que l&#39;inculp&eacute; ait &eacute;t&eacute; mis en pr&eacute;sence de ses accusateurs, et qu&#39;il ait eu la facult&eacute; de se d&eacute;fendre sur les choses dont on l&#39;accuse.</p>

<p><sup class="versenum">17&nbsp;</sup>Ils sont donc venus ici, et, sans diff&eacute;rer, je m&#39;assis le lendemain sur mon tribunal, et je donnai l&#39;ordre qu&#39;on amen&acirc;t cet homme.</p>

<p><sup class="versenum">18&nbsp;</sup>Les accusateurs, s&#39;&eacute;tant pr&eacute;sent&eacute;s, ne lui imput&egrave;rent rien de ce que je supposais;</p>

<p><sup class="versenum">19&nbsp;</sup>ils avaient avec lui des discussions relatives &agrave; leur religion particuli&egrave;re, et &agrave; un certain J&eacute;sus qui est mort, et que Paul affirmait &ecirc;tre vivant.</p>

<p><sup class="versenum">20&nbsp;</sup>Ne sachant quel parti prendre dans ce d&eacute;bat, je lui demandai s&#39;il voulait aller &agrave; J&eacute;rusalem, et y &ecirc;tre jug&eacute; sur ces choses.</p>

<p><sup class="versenum">21&nbsp;</sup>Mais Paul en ayant appel&eacute;, pour que sa cause f&ucirc;t r&eacute;serv&eacute;e &agrave; la connaissance de l&#39;empereur, j&#39;ai ordonn&eacute; qu&#39;on le gard&acirc;t jusqu&#39;&agrave; ce que je l&#39;envoyasse &agrave; C&eacute;sar.</p>

<p><sup class="versenum">22&nbsp;</sup>Agrippa dit &agrave; Festus: Je voudrais aussi entendre cet homme. Demain, r&eacute;pondit Festus, tu l&#39;entendras.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/349.mp4" type="button" class="external-movie">
         Regardez Actes 25:1-22 </button>
    <div class="collapsed"></div>




<h2>Discussion de d&eacute;couverte</h2>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ? Pourquoi ?</li>
	<li>&Agrave; ce niveau de l&rsquo;histoire, qu&rsquo;est-ce qui est nouveau ou est d&eacute;velopp&eacute; ?</li>
	<li>Quel mod&egrave;le a &eacute;t&eacute; donn&eacute; quant &agrave; la vie d&eacute;pendante de l&rsquo;Esprit, faire de disciples ou au leadership ?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire?</li>
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


<p><em>Des questions suppl&eacute;mentaires dont vous pouvez faire usage:</em></p>

<ul>
	<li>Comment les disciples de J&eacute;sus poursuivent-ils Son &oelig;uvre de faire des disciples et d&rsquo;implantation d&rsquo;&eacute;glises ?</li>
	<li>Comment l&rsquo;&eacute;vangile impacte-t-il les gens et la soci&eacute;t&eacute; ?</li>
	<li>Quels &eacute;taient les barri&egrave;res et les obstacles qui ont &eacute;t&eacute; surmont&eacute;s et comment ont-ils &eacute;t&eacute; surmont&eacute;s ?</li>
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


<h2>Lire, raconter et corriger</h2>

<p>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</p>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<p>Le gouverneur F&eacute;lix a gard&eacute; Paul en prison pendant deux ans et a transmis son dossier au nouveau gouverneur, Festus, pour qu&#39;il s&#39;en occupe. Les leaders religieux juifs ont saisi l&rsquo;occasion de la visite de Festus &agrave; J&eacute;rusalem pour enfin obtenir Paul. Si le proc&egrave;s pouvait &ecirc;tre ramen&eacute; &agrave; J&eacute;rusalem, ils auraient une autre chance d&#39;assassiner Paul au cours des deux jours de voyage. Suspectant leur plan, Paul a exhort&eacute; le gouverneur &agrave; respecter la loi romaine et &agrave; ne pas c&eacute;der pour plaire aux dirigeants juifs. Ayant d&eacute;j&agrave; &eacute;t&eacute; injustement d&eacute;tenu pendant deux ans, il a us&eacute; de son droit en tant que citoyen romain de faire entendre sa cause devant C&eacute;sar.</p>

<p>Paul a soutenu que suivre J&eacute;sus &eacute;tait conforme &agrave; la fois avec son identit&eacute; de juif et de citoyen loyal de Rome. Lorsque le roi Agrippa et B&eacute;r&eacute;nice ont visit&eacute; C&eacute;sar&eacute;e, ils &eacute;taient int&eacute;ress&eacute;s &agrave; entendre Paul. J&eacute;sus conduit souverainement toutes ces circonstances pour accomplir sa promesse que Paul t&eacute;moignerait devant C&eacute;sar.</p>

<p>&nbsp;</p>
</div>

<p><em>Pratiquez ici la lib&eacute;ralit&eacute; et la sainte-c&egrave;ne ou dans la section Se pr&eacute;parer pour la mission.</em></p>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary4" class="summary"><h2>+ Se pr&eacute;parer pour la mission</h2></div>
<div class="collapsed" id ="Text4">
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

<h2>Aller en mission</h2>

<ul>
	<li>Identifiez des gens vers qui ou des endroits o&ugrave; vous pouvez prendre l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>&Eacute;crivez des promesses &laquo; Je ferai d&rsquo;ici quand &raquo; et partagez cela avec votre petit groupe.</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note3Text')"
        id="note3Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Prier pour la mission</h2>

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</p>

<h2>B&eacute;n&eacute;diction (facultatif)</h2>
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

			<td class="social" @click="share('lesson', 'Paul présente sa défense devant le nouveau gouverneur romain Festus: ', '/content/M2/fra/multiply3/multiply349.html')">
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