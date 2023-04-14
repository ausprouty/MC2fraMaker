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
                        <div class="chapter_number ltr"><h1>46.</h1></div>
                        <div class="chapter_title ltr"><h1>Paul questionné par les autorités</h1></div>
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
	<li>Lisez ou observez Actes 22:22-23:11 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 22:22-23:11</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">22&nbsp;</sup>Ils l&#39;&eacute;cout&egrave;rent jusqu&#39;&agrave; cette parole. Mais alors ils &eacute;lev&egrave;rent la voix, disant: Ote de la terre un pareil homme! Il n&#39;est pas digne de vivre.</p>

<p><sup class="versenum">23&nbsp;</sup>Et ils poussaient des cris, jetaient leurs v&ecirc;tements, lan&ccedil;aient de la poussi&egrave;re en l&#39;air.</p>

<p><sup class="versenum">24&nbsp;</sup>Le tribun commanda de faire entrer Paul dans la forteresse, et de lui donner la question par le fouet, afin de savoir pour quel motif ils criaient ainsi contre lui.</p>

<p><sup class="versenum">25&nbsp;</sup>Lorsqu&#39;on l&#39;eut expos&eacute; au fouet, Paul dit au centenier qui &eacute;tait pr&eacute;sent: Vous est-il permis de battre de verges un citoyen romain, qui n&#39;est pas m&ecirc;me condamn&eacute;?</p>

<p><sup class="versenum">26&nbsp;</sup>A ces mots, le centenier alla vers le tribun pour l&#39;avertir, disant: Que vas-tu faire? Cet homme est Romain.</p>

<p><sup class="versenum">27&nbsp;</sup>Et le tribun, &eacute;tant venu, dit &agrave; Paul: Dis-moi, es-tu Romain? Oui, r&eacute;pondit-il.</p>

<p><sup class="versenum">28&nbsp;</sup>Le tribun reprit: C&#39;est avec beaucoup d&#39;argent que j&#39;ai acquis ce droit de citoyen. Et moi, dit Paul, je l&#39;ai par ma naissance.</p>

<p><sup class="versenum">29&nbsp;</sup>Aussit&ocirc;t ceux qui devaient lui donner la question se retir&egrave;rent, et le tribun, voyant que Paul &eacute;tait Romain, fut dans la crainte parce qu&#39;il l&#39;avait fait lier.</p>

<p><sup class="versenum">30&nbsp;</sup>Le lendemain, voulant savoir avec certitude de quoi les Juifs l&#39;accusaient, le tribun lui fit &ocirc;ter ses liens, et donna l&#39;ordre aux principaux sacrificateurs et &agrave; tout le sanh&eacute;drin de se r&eacute;unir; puis, faisant descendre Paul, il le pla&ccedil;a au milieu d&#39;eux.</p>

<p><sup class="versenum">1 </sup>Paul, les regards fix&eacute;s sur le sanh&eacute;drin, dit: Hommes fr&egrave;res, c&#39;est en toute bonne conscience que je me suis conduit jusqu&#39;&agrave; ce jour devant Dieu...</p>

<p><sup class="versenum">2&nbsp;</sup>Le souverain sacrificateur Ananias ordonna &agrave; ceux qui &eacute;taient pr&egrave;s de lui de le frapper sur la bouche.</p>

<p><sup class="versenum">3&nbsp;</sup>Alors Paul lui dit: Dieu te frappera, muraille blanchie! Tu es assis pour me juger selon la loi, et tu violes la loi en ordonnant qu&#39;on me frappe!</p>

<p><sup class="versenum">4&nbsp;</sup>Ceux qui &eacute;taient pr&egrave;s de lui dirent: Tu insultes le souverain sacrificateur de Dieu!</p>

<p><sup class="versenum">5&nbsp;</sup>Et Paul dit: Je ne savais pas, fr&egrave;res, que ce f&ucirc;t le souverain sacrificateur; car il est &eacute;crit: Tu ne parleras pas mal du chef de ton peuple.</p>

<p><sup class="versenum">6&nbsp;</sup>Paul, sachant qu&#39;une partie de l&#39;assembl&eacute;e &eacute;tait compos&eacute;e de sadduc&eacute;ens et l&#39;autre de pharisiens, s&#39;&eacute;cria dans le sanh&eacute;drin: Hommes fr&egrave;res, je suis pharisien, fils de pharisien; c&#39;est &agrave; cause de l&#39;esp&eacute;rance et de la r&eacute;surrection des morts que je suis mis en jugement.</p>

<p><sup class="versenum">7&nbsp;</sup>Quand il eut dit cela, il s&#39;&eacute;leva une discussion entre les pharisiens et les sadduc&eacute;ens, et l&#39;assembl&eacute;e se divisa.</p>

<p><sup class="versenum">8&nbsp;</sup>Car les sadduc&eacute;ens disent qu&#39;il n&#39;y a point de r&eacute;surrection, et qu&#39;il n&#39;existe ni ange ni esprit, tandis que les pharisiens affirment les deux choses.</p>

<p><sup class="versenum">9&nbsp;</sup>Il y eut une grande clameur, et quelques scribes du parti des pharisiens, s&#39;&eacute;tant lev&eacute;s, engag&egrave;rent un vif d&eacute;bat, et dirent: Nous ne trouvons aucun mal en cet homme; peut-&ecirc;tre un esprit ou un ange lui a-t-il parl&eacute;.</p>

<p><sup class="versenum">10&nbsp;</sup>Comme la discorde allait croissant, le tribun craignant que Paul ne f&ucirc;t mis en pi&egrave;ces par ces gens, fit descendre les soldats pour l&#39;enlever du milieu d&#39;eux et le conduire &agrave; la forteresse.</p>

<p><sup class="versenum">11&nbsp;</sup>La nuit suivante, le Seigneur apparut &agrave; Paul, et dit: Prends courage; car, de m&ecirc;me que tu as rendu t&eacute;moignage de moi dans J&eacute;rusalem, il faut aussi que tu rendes t&eacute;moignage dans Rome.</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/346.mp4" type="button" class="external-movie">
         Regardez Actes 22:22-23:11 </button>
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

<ul>
	<li class="nobreak-final-final">En tant que citoyen romain, Paul &eacute;tait prot&eacute;g&eacute; par le tribun, mais il &eacute;tait toujours en grand danger. Le tribun romain a fait preuve d&#39;int&eacute;grit&eacute; en cherchant &agrave; comprendre la situation et &agrave; suivre le droit civil romain. Les Juifs &eacute;taient tr&egrave;s z&eacute;l&eacute;s au sujet de leurs croyances religieuses, pr&ecirc;ts &agrave; tuer ceux qui avaient une croyance contraire ou, dans leur compr&eacute;hension, &laquo;offensaient&raquo; Dieu. Paul a profit&eacute; des diff&eacute;rences th&eacute;ologiques qu&rsquo;il y a entre les dirigeants juifs pour d&eacute;tourner l&#39;attention de lui-m&ecirc;me vers leur d&eacute;saccord th&eacute;ologique. J&eacute;sus est apparu &agrave; Paul pour l&#39;encourager disant qu&rsquo;Il &oelig;uvre &agrave; travers lui, malgr&eacute; la r&eacute;ponse hostile des chefs religieux juifs. Pendant que nous poursuivons l&#39;expansion du Royaume de Dieu, J&eacute;sus tient sa promesse de &laquo;ne jamais nous d&eacute;laisser ni nous abandonner&raquo;. (<span class="popup-link" @click = "popUp('pop5')"> Matthieu 28:20</span>).&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">20&nbsp;</sup>et enseignez-leur &agrave; observer tout ce que je vous ai prescrit. Et voici, je suis avec vous tous les jours, jusqu&#39;&agrave; la fin du monde.</p>

	<p>&nbsp;</p>
	<!-- end bible --></div>
	Lisez<span class="popup-link" @click = "popUp('pop4')">  &Eacute;ph&eacute;siens 2:10</span>.&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">10&nbsp;</sup>Car nous sommes son ouvrage, ayant &eacute;t&eacute; cr&eacute;&eacute;s en J&eacute;sus Christ pour de bonnes oeuvres, que Dieu a pr&eacute;par&eacute;es d&#39;avance, afin que nous les pratiquions.</p>
	<!-- end bible --></div>
	Comme Paul, le Seigneur a cr&eacute;&eacute; chacun de nous pour de bonnes &oelig;uvres et il utilise souverainement toutes nos exp&eacute;riences pour accomplir les &oelig;uvres qu&#39;Il a pr&eacute;par&eacute;es pour nous.</li>
</ul>

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

			<td class="social" @click="share('lesson', 'Paul questionné par les autorités: ', '/content/M2/fra/multiply3/multiply346.html')">
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