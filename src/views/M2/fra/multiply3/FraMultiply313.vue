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
                        <div class="chapter_number ltr"><h1>13.</h1></div>
                        <div class="chapter_title ltr"><h1>Étienne fut tué et les croyants se sont dispersés</h1></div>
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
	<li>Lisez ou observez Actes 7:54-8:3 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 7:54-8:3</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">54&nbsp;</sup>En entendant ces paroles, ils &eacute;taient furieux dans leur coeur, et ils grin&ccedil;aient des dents contre lui.</p>

<p><sup class="versenum">55&nbsp;</sup>Mais &Eacute;tienne, rempli du Saint Esprit, et fixant les regards vers le ciel, vit la gloire de Dieu et J&eacute;sus debout &agrave; la droite de Dieu.</p>

<p><sup class="versenum">56&nbsp;</sup>Et il dit: Voici, je vois les cieux ouverts, et le Fils de l&#39;homme debout &agrave; la droite de Dieu.</p>

<p><sup class="versenum">57&nbsp;</sup>Ils pouss&egrave;rent alors de grands cris, en se bouchant les oreilles, et ils se pr&eacute;cipit&egrave;rent tous ensemble sur lui,</p>

<p><sup class="versenum">58&nbsp;</sup>le tra&icirc;n&egrave;rent hors de la ville, et le lapid&egrave;rent. Les t&eacute;moins d&eacute;pos&egrave;rent leurs v&ecirc;tements aux pieds d&#39;un jeune homme nomm&eacute; Saul.</p>

<p><sup class="versenum">59&nbsp;</sup>Et ils lapidaient &Eacute;tienne, qui priait et disait: Seigneur J&eacute;sus, re&ccedil;ois mon esprit!</p>

<p><sup class="versenum">60&nbsp;</sup>Puis, s&#39;&eacute;tant mis &agrave; genoux, il s&#39;&eacute;cria d&#39;une voix forte: Seigneur, ne leur impute pas ce p&eacute;ch&eacute;! Et, apr&egrave;s ces paroles, il s&#39;endormit.</p>

<p><sup class="versenum">1 </sup>Saul avait approuv&eacute; le meurtre d&#39;&Eacute;tienne. Il y eut, ce jour-l&agrave;, une grande pers&eacute;cution contre l&#39;&Eacute;glise de J&eacute;rusalem; et tous, except&eacute; les ap&ocirc;tres, se dispers&egrave;rent dans les contr&eacute;es de la Jud&eacute;e et de la Samarie.</p>

<p><sup class="versenum">2&nbsp;</sup>Des hommes pieux ensevelirent &Eacute;tienne, et le pleur&egrave;rent &agrave; grand bruit.</p>

<p><sup class="versenum">3&nbsp;</sup>Saul, de son c&ocirc;t&eacute;, ravageait l&#39;&Eacute;glise; p&eacute;n&eacute;trant dans les maisons, il en arrachait hommes et femmes, et les faisait jeter en prison.</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/313.mp4" type="button" class="external-movie">
         Regardez Actes 7:54-8:3 </button>
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

<p>&Eacute;tienne a montr&eacute; ses comp&eacute;tences dans la maitrise de la Parole de Dieu &nbsp;et a affront&eacute; les leaders avec les paroles de v&eacute;rit&eacute;. Il les a accus&eacute;s de d&eacute;sob&eacute;ir &agrave; Dieu, en p&eacute;chant contre l&rsquo;Esprit-Saint, la loi, et J&eacute;sus le Messie. Quand &Eacute;tienne leur a dit qu&rsquo;il a vu J&eacute;sus, &laquo; le Fils de l&rsquo;Homme &raquo;; les leaders &eacute;taient en &eacute;ruption de violence contre lui. J&eacute;sus a enseign&eacute; aux disciples que ceux qui les ont tu&eacute;, ils &nbsp;pensaient servir Dieu (<span class="popup-link" @click = "popUp('pop3')"> Matthieu 10:16-39</span>).&nbsp;</p>

<div class="popup invisible" id="pop3"><!-- begin bible -->
<p><sup class="versenum">16&nbsp;</sup>Voici, je vous envoie comme des brebis au milieu des loups. Soyez donc prudents comme les serpents, et simples comme les colombes.</p>

<p><sup class="versenum">17&nbsp;</sup>Mettez-vous en garde contre les hommes; car ils vous livreront aux tribunaux, et ils vous battront de verges dans leurs synagogues;</p>

<p><sup class="versenum">18&nbsp;</sup>vous serez men&eacute;s, &agrave; cause de moi, devant des gouverneurs et devant des rois, pour servir de t&eacute;moignage &agrave; eux et aux pa&iuml;ens.</p>

<p><sup class="versenum">19&nbsp;</sup>Mais, quand on vous livrera, ne vous inqui&eacute;tez ni de la mani&egrave;re dont vous parlerez ni de ce que vous direz: ce que vous aurez &agrave; dire vous sera donn&eacute; &agrave; l&#39;heure m&ecirc;me;</p>

<p><sup class="versenum">20&nbsp;</sup>car ce n&#39;est pas vous qui parlerez, c&#39;est l&#39;Esprit de votre P&egrave;re qui parlera en vous.</p>

<p><sup class="versenum">21&nbsp;</sup>Le fr&egrave;re livrera son fr&egrave;re &agrave; la mort, et le p&egrave;re son enfant; les enfants se soul&egrave;veront contre leurs parents, et les feront mourir.</p>

<p><sup class="versenum">22&nbsp;</sup>Vous serez ha&iuml;s de tous, &agrave; cause de mon nom; mais celui qui pers&eacute;v&eacute;rera jusqu&#39;&agrave; la fin sera sauv&eacute;.</p>

<p><sup class="versenum">23&nbsp;</sup>Quand on vous pers&eacute;cutera dans une ville, fuyez dans une autre. Je vous le dis en v&eacute;rit&eacute;, vous n&#39;aurez pas achev&eacute; de parcourir les villes d&#39;Isra&euml;l que le Fils de l&#39;homme sera venu.</p>

<p><sup class="versenum">24&nbsp;</sup>Le disciple n&#39;est pas plus que le ma&icirc;tre, ni le serviteur plus que son seigneur.</p>

<p><sup class="versenum">25&nbsp;</sup>Il suffit au disciple d&#39;&ecirc;tre trait&eacute; comme son ma&icirc;tre, et au serviteur comme son seigneur. S&#39;ils ont appel&eacute; le ma&icirc;tre de la maison B&eacute;elz&eacute;bul, &agrave; combien plus forte raison appelleront-ils ainsi les gens de sa maison!</p>

<p><sup class="versenum">26&nbsp;</sup>Ne les craignez donc point; car il n&#39;y a rien de cach&eacute; qui ne doive &ecirc;tre d&eacute;couvert, ni de secret qui ne doive &ecirc;tre connu.</p>

<p><sup class="versenum">27&nbsp;</sup>Ce que je vous dis dans les t&eacute;n&egrave;bres, dites-le en plein jour; et ce qui vous est dit &agrave; l&#39;oreille, pr&ecirc;chez-le sur les toits.</p>

<p><sup class="versenum">28&nbsp;</sup>Ne craignez pas ceux qui tuent le corps et qui ne peuvent tuer l&#39;&acirc;me; craignez plut&ocirc;t celui qui peut faire p&eacute;rir l&#39;&acirc;me et le corps dans la g&eacute;henne.</p>

<p><sup class="versenum">29&nbsp;</sup>Ne vend-on pas deux passereaux pour un sou? Cependant, il n&#39;en tombe pas un &agrave; terre sans la volont&eacute; de votre P&egrave;re.</p>

<p><sup class="versenum">30&nbsp;</sup>Et m&ecirc;me les cheveux de votre t&ecirc;te sont tous compt&eacute;s.</p>

<p><sup class="versenum">31&nbsp;</sup>Ne craignez donc point: vous valez plus que beaucoup de passereaux.</p>

<p><sup class="versenum">32&nbsp;</sup>C&#39;est pourquoi, quiconque me confessera devant les hommes, je le confesserai aussi devant mon P&egrave;re qui est dans les cieux;</p>

<p><sup class="versenum">33&nbsp;</sup>mais quiconque me reniera devant les hommes, je le renierai aussi devant mon P&egrave;re qui est dans les cieux.</p>

<p><sup class="versenum">34&nbsp;</sup>Ne croyez pas que je sois venu apporter la paix sur la terre; je ne suis pas venu apporter la paix, mais l&#39;&eacute;p&eacute;e.</p>

<p><sup class="versenum">35&nbsp;</sup>Car je suis venu mettre la division entre l&#39;homme et son p&egrave;re, entre la fille et sa m&egrave;re, entre la belle-fille et sa belle-m&egrave;re;</p>

<p><sup class="versenum">36&nbsp;</sup>et l&#39;homme aura pour ennemis les gens de sa maison.</p>

<p><sup class="versenum">37&nbsp;</sup>Celui qui aime son p&egrave;re ou sa m&egrave;re plus que moi n&#39;est pas digne de moi, et celui qui aime son fils ou sa fille plus que moi n&#39;est pas digne de moi;</p>

<p><sup class="versenum">38&nbsp;</sup>celui qui ne prend pas sa croix, et ne me suit pas, n&#39;est pas digne de moi.</p>

<p><sup class="versenum">39&nbsp;</sup>Celui qui conservera sa vie la perdra, et celui qui perdra sa vie &agrave; cause de moi la retrouvera.</p>
<!-- end bible --></div>
J&eacute;sus a &eacute;t&eacute; vu debout (non assis) &agrave; la place de gloire &agrave; cot&eacute; de Dieu le P&egrave;re qui veille sur tous ces &eacute;v&egrave;nements, mais il n&rsquo;a pas sauv&eacute; &Eacute;tienne de la mort. &Eacute;tienne a pri&eacute; directement J&eacute;sus lorsqu&rsquo;il mourait et sa demande montrait qu&rsquo;il a compris l&rsquo;&eacute;galit&eacute; de J&eacute;sus avec le P&egrave;re (<span class="popup-link" @click = "popUp('pop4')"> Actes 7 :59-60</span>).

<div class="popup invisible" id="pop4"><!-- begin bible -->
<p><sup class="versenum">59&nbsp;</sup>Et ils lapidaient &Eacute;tienne, qui priait et disait: Seigneur J&eacute;sus, re&ccedil;ois mon esprit!</p>

<p><sup class="versenum">60&nbsp;</sup>Puis, s&#39;&eacute;tant mis &agrave; genoux, il s&#39;&eacute;cria d&#39;une voix forte: Seigneur, ne leur impute pas ce p&eacute;ch&eacute;! Et, apr&egrave;s ces paroles, il s&#39;endormit.</p>
<!-- end bible --></div>
Cette histoire pr&eacute;sente aussi un jeune leader religieux nomm&eacute; Saul qui a approuv&eacute; tout ce qui &eacute;tait pass&eacute;. Saul a commenc&eacute; par aller partout pour d&eacute;truire l&rsquo;&eacute;glise. Hommes et femmes ont &eacute;t&eacute; pers&eacute;cut&eacute;s pour leur foi et beaucoup de croyants ont quitt&eacute; J&eacute;rusalem pour fuir la violence.

<p>&nbsp;</p>

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

			<td class="social" @click="share('lesson', 'Étienne fut tué et les croyants se sont dispersés: ', '/content/M2/fra/multiply3/multiply313.html')">
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