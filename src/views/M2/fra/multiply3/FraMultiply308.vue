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
                        <div class="chapter_number ltr"><h1>8.</h1></div>
                        <div class="chapter_title ltr"><h1>Suivre le c'ur de Jésus avec intégrité</h1></div>
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
	<li>Lisez ou observez Actes 4:32-5:11 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 4:32-5:11</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">32&nbsp;</sup>La multitude de ceux qui avaient cru n&#39;&eacute;tait qu&#39;un coeur et qu&#39;une &acirc;me. Nul ne disait que ses biens lui appartinssent en propre, mais tout &eacute;tait commun entre eux.</p>

<p><sup class="versenum">33&nbsp;</sup>Les ap&ocirc;tres rendaient avec beaucoup de force t&eacute;moignage de la r&eacute;surrection du Seigneur J&eacute;sus. Et une grande gr&acirc;ce reposait sur eux tous.</p>

<p><sup class="versenum">34&nbsp;</sup>Car il n&#39;y avait parmi eux aucun indigent: tous ceux qui poss&eacute;daient des champs ou des maisons les vendaient, apportaient le prix de ce qu&#39;ils avaient vendu,</p>

<p><sup class="versenum">35&nbsp;</sup>et le d&eacute;posaient aux pieds des ap&ocirc;tres; et l&#39;on faisait des distributions &agrave; chacun selon qu&#39;il en avait besoin.</p>

<p><sup class="versenum">36&nbsp;</sup>Joseph, surnomm&eacute; par les ap&ocirc;tres Barnabas, ce qui signifie fils d&#39;exhortation, L&eacute;vite, originaire de Chypre,</p>

<p><sup class="versenum">37&nbsp;</sup>vendit un champ qu&#39;il poss&eacute;dait, apporta l&#39;argent, et le d&eacute;posa aux pieds des ap&ocirc;tres.</p>

<p><sup class="versenum">1 </sup>Mais un homme nomm&eacute; Ananias, avec Saphira sa femme, vendit une propri&eacute;t&eacute;,</p>

<p><sup class="versenum">2&nbsp;</sup>et retint une partie du prix, sa femme le sachant; puis il apporta le reste, et le d&eacute;posa aux pieds des ap&ocirc;tres.</p>

<p><sup class="versenum">3&nbsp;</sup>Pierre lui dit: Ananias, pourquoi Satan a-t-il rempli ton coeur, au point que tu mentes au Saint Esprit, et que tu aies retenu une partie du prix du champ?</p>

<p><sup class="versenum">4&nbsp;</sup>S&#39;il n&#39;e&ucirc;t pas &eacute;t&eacute; vendu, ne te restait-il pas? Et, apr&egrave;s qu&#39;il a &eacute;t&eacute; vendu, le prix n&#39;&eacute;tait-il pas &agrave; ta disposition? Comment as-tu pu mettre en ton coeur un pareil dessein? Ce n&#39;est pas &agrave; des hommes que tu as menti, mais &agrave; Dieu.</p>

<p><sup class="versenum">5&nbsp;</sup>Ananias, entendant ces paroles, tomba, et expira. Une grande crainte saisit tous les auditeurs.</p>

<p><sup class="versenum">6&nbsp;</sup>Les jeunes gens, s&#39;&eacute;tant lev&eacute;s, l&#39;envelopp&egrave;rent, l&#39;emport&egrave;rent, et l&#39;ensevelirent.</p>

<p><sup class="versenum">7&nbsp;</sup>Environ trois heures plus tard, sa femme entra, sans savoir ce qui &eacute;tait arriv&eacute;.</p>

<p><sup class="versenum">8&nbsp;</sup>Pierre lui adressa la parole: Dis-moi, est-ce &agrave; un tel prix que vous avez vendu le champ? Oui, r&eacute;pondit-elle, c&#39;est &agrave; ce prix-l&agrave;.</p>

<p><sup class="versenum">9&nbsp;</sup>Alors Pierre lui dit: Comment vous &ecirc;tes-vous accord&eacute;s pour tenter l&#39;Esprit du Seigneur? Voici, ceux qui ont enseveli ton mari sont &agrave; la porte, et ils t&#39;emporteront.</p>

<p><sup class="versenum">10&nbsp;</sup>Au m&ecirc;me instant, elle tomba aux pieds de l&#39;ap&ocirc;tre, et expira. Les jeunes gens, &eacute;tant entr&eacute;s, la trouv&egrave;rent morte; ils l&#39;emport&egrave;rent, et l&#39;ensevelirent aupr&egrave;s de son mari.</p>

<p><sup class="versenum">11&nbsp;</sup>Une grande crainte s&#39;empara de toute l&#39;assembl&eacute;e et de tous ceux qui apprirent ces choses.</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/308.mp4" type="button" class="external-movie">
         Regardez Actes 4:32-5:11 </button>
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
	<li class="nobreak-final-final" style="text-align:justify">Les croyants avaient une communaut&eacute; empreinte d&rsquo;amour. Ils partageaient avec hardiesse leur foi et se sacrifiaient pour prendre soin les uns des autres. Nous voyons comment un homme de Chypre, Joseph appel&eacute; Barnabas, a g&eacute;n&eacute;reusement vendu des terres qu&#39;il poss&eacute;dait pour aider &agrave; r&eacute;pondre aux besoins des autres dans l&#39;&eacute;glise. Mais &eacute;galement nous voyons comment un couple a essay&eacute; de tromper l&#39;&eacute;glise. Leur motivation n&#39;&eacute;tait pas d&#39;aider les pauvres, mais d&#39;accro&icirc;tre leur r&eacute;putation de g&eacute;n&eacute;reux et spirituel parmi les croyants. Le Seigneur est intervenu pour ne pas permettre &agrave; l&#39;hypocrisie d&#39;Ananias et de Saphira de se r&eacute;pandre. Nous apprenons que mentir au Saint-Esprit &eacute;quivaut &agrave; mentir &agrave; Dieu, ce qui rend le Saint-Esprit &eacute;gal &agrave; Dieu (<span class="popup-link" @click = "popUp('pop3')"> Actes 5:3-4</span>).

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">3&nbsp;</sup>Pierre lui dit: Ananias, pourquoi Satan a-t-il rempli ton coeur, au point que tu mentes au Saint Esprit, et que tu aies retenu une partie du prix du champ?</p>

	<p><sup class="versenum">4&nbsp;</sup>S&#39;il n&#39;e&ucirc;t pas &eacute;t&eacute; vendu, ne te restait-il pas? Et, apr&egrave;s qu&#39;il a &eacute;t&eacute; vendu, le prix n&#39;&eacute;tait-il pas &agrave; ta disposition? Comment as-tu pu mettre en ton coeur un pareil dessein? Ce n&#39;est pas &agrave; des hommes que tu as menti, mais &agrave; Dieu.</p>
	<!-- end bible --></div>
	&nbsp;M&ecirc;me si nous avons le privil&egrave;ge d&rsquo;une relation personnelle avec un Dieu saint &agrave; travers J&eacute;sus, cet incident unique du jugement de Dieu a rappel&eacute; aux croyants d&rsquo;avoir un v&eacute;ritable respect pour le Seigneur. Pendant que nous recherchons le c&oelig;ur du Seigneur en vue de r&eacute;pondre aux besoins des autres, nous devons le faire avec int&eacute;grit&eacute;.</li>
</ul>

<p class="MultiplyInstruction" style="text-align:justify">&nbsp;</p>
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

			<td class="social" @click="share('lesson', 'Suivre le c\'ur de Jésus avec intégrité: ', '/content/M2/fra/multiply3/multiply308.html')">
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