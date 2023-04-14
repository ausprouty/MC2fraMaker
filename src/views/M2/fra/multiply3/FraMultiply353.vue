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
                        <div class="chapter_number ltr"><h1>53.</h1></div>
                        <div class="chapter_title ltr"><h1>Ministère en étant sur l'île de Malte</h1></div>
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
	<li>Lisez ou observez Actes 28:1-10 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 28:1-10</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Apr&egrave;s nous &ecirc;tre sauv&eacute;s, nous reconn&ucirc;mes que l&#39;&icirc;le s&#39;appelait Malte.</p>

<p><sup class="versenum">2&nbsp;</sup>Les barbares nous t&eacute;moign&egrave;rent une bienveillance peu commune; ils nous recueillirent tous aupr&egrave;s d&#39;un grand feu, qu&#39;ils avaient allum&eacute; parce que la pluie tombait et qu&#39;il faisait grand froid.</p>

<p><sup class="versenum">3&nbsp;</sup>Paul ayant ramass&eacute; un tas de broussailles et l&#39;ayant mis au feu, une vip&egrave;re en sortit par l&#39;effet de la chaleur et s&#39;attacha &agrave; sa main.</p>

<p><sup class="versenum">4&nbsp;</sup>Quand les barbares virent l&#39;animal suspendu &agrave; sa main, ils se dirent les uns aux autres: Assur&eacute;ment cet homme est un meurtrier, puisque la Justice n&#39;a pas voulu le laisser vivre, apr&egrave;s qu&#39;il a &eacute;t&eacute; sauv&eacute; de la mer.</p>

<p><sup class="versenum">5&nbsp;</sup>Paul secoua l&#39;animal dans le feu, et ne ressentit aucun mal.</p>

<p><sup class="versenum">6&nbsp;</sup>Ces gens s&#39;attendaient &agrave; le voir enfler ou tomber mort subitement; mais, apr&egrave;s avoir longtemps attendu, voyant qu&#39;il ne lui arrivait aucun mal, ils chang&egrave;rent d&#39;avis et dirent que c&#39;&eacute;tait un dieu.</p>

<p><sup class="versenum">7&nbsp;</sup>Il y avait, dans les environs, des terres appartenant au principal personnage de l&#39;&icirc;le, nomm&eacute; Publius, qui nous re&ccedil;ut et nous logea pendant trois jours de la mani&egrave;re la plus amicale.</p>

<p><sup class="versenum">8&nbsp;</sup>Le p&egrave;re de Publius &eacute;tait alors au lit, malade de la fi&egrave;vre et de la dysenterie; Paul, s&#39;&eacute;tant rendu vers lui, pria, lui imposa les mains, et le gu&eacute;rit.</p>

<p><sup class="versenum">9&nbsp;</sup>L&agrave;-dessus, vinrent les autres malades de l&#39;&icirc;le, et ils furent gu&eacute;ris.</p>

<p><sup class="versenum">10&nbsp;</sup>On nous rendit de grands honneurs, et, &agrave; notre d&eacute;part, on nous fournit les choses dont nous avions besoin.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/353.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 28:1-10&nbsp; </button>
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
	<li class="nobreak-final-final">Lisez <span class="popup-link" @click = "popUp('pop3')"> Romains 8: 28-39</span>.&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">28&nbsp;</sup>Nous savons, du reste, que toutes choses concourent au bien de ceux qui aiment Dieu, de ceux qui sont appel&eacute;s selon son dessein.</p>

	<p><sup class="versenum">29&nbsp;</sup>Car ceux qu&#39;il a connus d&#39;avance, il les a aussi pr&eacute;destin&eacute;s &agrave; &ecirc;tre semblables &agrave; l&#39;image de son Fils, afin que son Fils f&ucirc;t le premier-n&eacute; entre plusieurs fr&egrave;res.</p>

	<p><sup class="versenum">30&nbsp;</sup>Et ceux qu&#39;il a pr&eacute;destin&eacute;s, il les a aussi appel&eacute;s; et ceux qu&#39;il a appel&eacute;s, il les a aussi justifi&eacute;s; et ceux qu&#39;il a justifi&eacute;s, il les a aussi glorifi&eacute;s.</p>

	<p><sup class="versenum">31&nbsp;</sup>Que dirons-nous donc &agrave; l&#39;&eacute;gard de ces choses? Si Dieu est pour nous, qui sera contre nous?</p>

	<p><sup class="versenum">32&nbsp;</sup>Lui, qui n&#39;a point &eacute;pargn&eacute; son propre Fils, mais qui l&#39;a livr&eacute; pour nous tous, comment ne nous donnera-t-il pas aussi toutes choses avec lui?</p>

	<p><sup class="versenum">33&nbsp;</sup>Qui accusera les &eacute;lus de Dieu? C&#39;est Dieu qui justifie!</p>

	<p><sup class="versenum">34&nbsp;</sup>Qui les condamnera? Christ est mort; bien plus, il est ressuscit&eacute;, il est &agrave; la droite de Dieu, et il interc&egrave;de pour nous!</p>

	<p><sup class="versenum">35&nbsp;</sup>Qui nous s&eacute;parera de l&#39;amour de Christ? Sera-ce la tribulation, ou l&#39;angoisse, ou la pers&eacute;cution, ou la faim, ou la nudit&eacute;, ou le p&eacute;ril, ou l&#39;&eacute;p&eacute;e?</p>

	<p><sup class="versenum">36&nbsp;</sup>selon qu&#39;il est &eacute;crit: C&#39;est &agrave; cause de toi qu&#39;on nous met &agrave; mort tout le jour, Qu&#39;on nous regarde comme des brebis destin&eacute;es &agrave; la boucherie.</p>

	<p><sup class="versenum">37&nbsp;</sup>Mais dans toutes ces choses nous sommes plus que vainqueurs par celui qui nous a aim&eacute;s.</p>

	<p><sup class="versenum">38&nbsp;</sup>Car j&#39;ai l&#39;assurance que ni la mort ni la vie, ni les anges ni les dominations, ni les choses pr&eacute;sentes ni les choses &agrave; venir,</p>

	<p><sup class="versenum">39&nbsp;</sup>ni les puissances, ni la hauteur, ni la profondeur, ni aucune autre cr&eacute;ature ne pourra nous s&eacute;parer de l&#39;amour de Dieu manifest&eacute; en J&eacute;sus Christ notre Seigneur.</p>
	<!-- end bible --></div>
	M&ecirc;me si, aux yeux de l&rsquo;homme, c&rsquo;&eacute;tait un arr&ecirc;t impr&eacute;vu et ind&eacute;sirable, cela faisait partie du plan souverain de Dieu. Quelles que soient les circonstances, Paul recherchait la bont&eacute; et le dessein de Dieu. Dans la d&eacute;pendance du Saint-Esprit, il &eacute;tait intentionnel dans ses relations et ob&eacute;issant au programme du Royaume de J&eacute;sus pendant qu&rsquo;il faisait le minist&egrave;re aupr&egrave;s de ceux qui l&rsquo;entouraient. Le Seigneur a m&ecirc;me prot&eacute;g&eacute; Paul de mani&egrave;re surnaturelle d&#39;une morsure de serpent venimeux. Le terrible d&eacute;sastre du naufrage s&#39;est av&eacute;r&eacute; &ecirc;tre une b&eacute;n&eacute;diction pour le peuple de Malte, et le Seigneur a re&ccedil;u la gloire. M&ecirc;me sur cette &icirc;le &eacute;loign&eacute;e, Paul a trouv&eacute; une personne de paix pr&eacute;par&eacute;e par Dieu, le principal personnage de l&rsquo;&iuml;le, Publius. La maison de Publius est devenue un centre de minist&egrave;re pendant les trois mois qu&#39;ils sont rest&eacute;s sur l&#39;&icirc;le. Publius &eacute;tait si reconnaissant au point o&ugrave; il fournit tout ce dont Paul, ses compagnons et les soldats avaient besoin pour se rendre &agrave; Rome. Le Seigneur a non seulement sauv&eacute; la vie de ceux qui ont fait naufrage et de ceux de l&#39;&icirc;le, mais il a &eacute;galement restaur&eacute; tout ce qui avait &eacute;t&eacute; perdu pendant la temp&ecirc;te.</li>
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

			<td class="social" @click="share('lesson', 'Ministère en étant sur l\'île de Malte: ', '/content/M2/fra/multiply3/multiply353.html')">
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