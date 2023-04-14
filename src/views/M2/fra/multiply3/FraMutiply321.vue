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
                        <div class="chapter_number ltr"><h1>21.</h1></div>
                        <div class="chapter_title ltr"><h1>Pierre explique ses actions</h1></div>
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
	<li>Lisez ou observez Actes 11:1-18 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 11:1-18</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Les ap&ocirc;tres et les fr&egrave;res qui &eacute;taient dans la Jud&eacute;e apprirent que les pa&iuml;ens avaient aussi re&ccedil;u la parole de Dieu.</p>

<p><sup class="versenum">2&nbsp;</sup>Et lorsque Pierre fut mont&eacute; &agrave; J&eacute;rusalem, les fid&egrave;les circoncis lui adress&egrave;rent des reproches,</p>

<p><sup class="versenum">3&nbsp;</sup>en disant: Tu es entr&eacute; chez des incirconcis, et tu as mang&eacute; avec eux.</p>

<p><sup class="versenum">4&nbsp;</sup>Pierre se mit &agrave; leur exposer d&#39;une mani&egrave;re suivie ce qui s&#39;&eacute;tait pass&eacute;.</p>

<p><sup class="versenum">5&nbsp;</sup>Il dit: J&#39;&eacute;tais dans la ville de Jopp&eacute;, et, pendant que je priais, je tombai en extase et j&#39;eus une vision: un objet, semblable &agrave; une grande nappe attach&eacute;e par les quatre coins, descendait du ciel et vint jusqu&#39;&agrave; moi.</p>

<p><sup class="versenum">6&nbsp;</sup>Les regards fix&eacute;s sur cette nappe, j&#39;examinai, et je vis les quadrup&egrave;des de la terre, les b&ecirc;tes sauvages, les reptiles, et les oiseaux du ciel.</p>

<p><sup class="versenum">7&nbsp;</sup>Et j&#39;entendis une voix qui me disait: L&egrave;ve-toi, Pierre, tue et mange.</p>

<p><sup class="versenum">8&nbsp;</sup>Mais je dis: Non, Seigneur, car jamais rien de souill&eacute; ni d&#39;impur n&#39;est entr&eacute; dans ma bouche.</p>

<p><sup class="versenum">9&nbsp;</sup>Et pour la seconde fois la voix se fit entendre du ciel: Ce que Dieu a d&eacute;clar&eacute; pur, ne le regarde pas comme souill&eacute;.</p>

<p><sup class="versenum">10&nbsp;</sup>Cela arriva jusqu&#39;&agrave; trois fois; puis tout fut retir&eacute; dans le ciel.</p>

<p><sup class="versenum">11&nbsp;</sup>Et voici, aussit&ocirc;t trois hommes envoy&eacute;s de C&eacute;sar&eacute;e vers moi se pr&eacute;sent&egrave;rent devant la porte de la maison o&ugrave; j&#39;&eacute;tais.</p>

<p><sup class="versenum">12&nbsp;</sup>L&#39;Esprit me dit de partir avec eux sans h&eacute;siter. Les six hommes que voici m&#39;accompagn&egrave;rent, et nous entr&acirc;mes dans la maison de Corneille.</p>

<p><sup class="versenum">13&nbsp;</sup>Cet homme nous raconta comment il avait vu dans sa maison l&#39;ange se pr&eacute;sentant &agrave; lui et disant: Envoie &agrave; Jopp&eacute;, et fais venir Simon, surnomm&eacute; Pierre,</p>

<p><sup class="versenum">14&nbsp;</sup>qui te dira des choses par lesquelles tu seras sauv&eacute;, toi et toute ta maison.</p>

<p><sup class="versenum">15&nbsp;</sup>Lorsque je me fus mis &agrave; parler, le Saint Esprit descendit sur eux, comme sur nous au commencement.</p>

<p><sup class="versenum">16&nbsp;</sup>Et je me souvins de cette parole du Seigneur: Jean a baptis&eacute; d&#39;eau, mais vous, vous serez baptis&eacute;s du Saint Esprit.</p>

<p><sup class="versenum">17&nbsp;</sup>Or, puisque Dieu leur a accord&eacute; le m&ecirc;me don qu&#39;&agrave; nous qui avons cru au Seigneur J&eacute;sus Christ, pouvais-je, moi, m&#39;opposer &agrave; Dieu?</p>

<p><sup class="versenum">18&nbsp;</sup>Apr&egrave;s avoir entendu cela, ils se calm&egrave;rent, et ils glorifi&egrave;rent Dieu, en disant: Dieu a donc accord&eacute; la repentance aussi aux pa&iuml;ens, afin qu&#39;ils aient la vie.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/321.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 11:1-18&nbsp; </button>
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
	<li class="nobreak-final-final">Les nouvelles sont rapidement remont&eacute;es &agrave; J&eacute;rusalem au sujet de la nouvelle &oelig;uvre op&eacute;r&eacute;e au sein des Pa&iuml;ens. Pierre retourne &agrave; J&eacute;rusalem apr&egrave;s sa tourn&eacute;e minist&eacute;rielle (<span class="popup-link" @click = "popUp('pop3')"> Actes 8:32</span>)&nbsp;

<div class="popup invisible" id="pop3"><!-- begin bible -->
<p><sup class="versenum">32&nbsp;</sup>Le passage de l&#39;&Eacute;criture qu&#39;il lisait &eacute;tait celui-ci: Il a &eacute;t&eacute; men&eacute; comme une brebis &agrave; la boucherie; Et, comme un agneau muet devant celui qui le tond, Il n&#39;a point ouvert la bouche.</p>
<!-- end bible --></div>
et les croyants juifs se sont attaqu&eacute;s &agrave; lui d&rsquo;avoir bris&eacute; les Lois Juives en entrant chez des pa&iuml;ens, en mangeant avec eux et m&ecirc;me en demeurant avec eux. Certains croyants n&rsquo;ont pas toujours compris les implications de la mission &eacute;vang&eacute;lique. Ils doutaient du c&oelig;ur du Seigneur pour les personnes non-juives. J&eacute;sus a utilis&eacute; cet &eacute;v&egrave;nement pour entamer le processus de briser l&rsquo;accent mis sur leur propre culture, et qui &nbsp;&eacute;tait une barri&egrave;re pour la mission globale qui consiste &agrave; faire de toutes les nations des disciples. C&rsquo;&eacute;tait la combinaison de la vision que Pierre a re&ccedil;ue ; l&rsquo;enseignement du Seigneur et la preuve de la pr&eacute;sence de l&rsquo;Esprit-Saint qui a prouv&eacute; qu&rsquo;en effet &nbsp;Dieu a accept&eacute; pleinement les pa&iuml;ens. Apr&egrave;s avoir entendu cela, les croyants Juifs ont finalement lou&eacute; le Seigneur pour avoir apport&eacute; le salut aux pa&iuml;ens. Leurs critiques et leurs inqui&eacute;tudes ce sont transform&eacute;es en adoration.

</li>
</ul>
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

			<td class="social" @click="share('lesson', 'Pierre explique ses actions: ', '/content/M2/fra/multiply3/mutiply321.html')">
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