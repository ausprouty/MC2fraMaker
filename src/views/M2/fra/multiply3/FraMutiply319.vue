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
                        <div class="chapter_number ltr"><h1>19.</h1></div>
                        <div class="chapter_title ltr"><h1>Jésus prépare les c'urs</h1></div>
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
	<li>Lisez ou observez Actes 10:1-33 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 10:1-33</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Il y avait &agrave; C&eacute;sar&eacute;e un homme nomm&eacute; Corneille, centenier dans la cohorte dite italienne.</p>

<p><sup class="versenum">2&nbsp;</sup>Cet homme &eacute;tait pieux et craignait Dieu, avec toute sa maison; il faisait beaucoup d&#39;aum&ocirc;nes au peuple, et priait Dieu continuellement.</p>

<p><sup class="versenum">3&nbsp;</sup>Vers la neuvi&egrave;me heure du jour, il vit clairement dans une vision un ange de Dieu qui entra chez lui, et qui lui dit: Corneille!</p>

<p><sup class="versenum">4&nbsp;</sup>Les regards fix&eacute;s sur lui, et saisi d&#39;effroi, il r&eacute;pondit: Qu&#39;est-ce, Seigneur? Et l&#39;ange lui dit: Tes pri&egrave;res et tes aum&ocirc;nes sont mont&eacute;es devant Dieu, et il s&#39;en est souvenu.</p>

<p><sup class="versenum">5&nbsp;</sup>Envoie maintenant des hommes &agrave; Jopp&eacute;, et fais venir Simon, surnomm&eacute; Pierre;</p>

<p><sup class="versenum">6&nbsp;</sup>il est log&eacute; chez un certain Simon, corroyeur, dont la maison est pr&egrave;s de la mer.</p>

<p><sup class="versenum">7&nbsp;</sup>D&egrave;s que l&#39;ange qui lui avait parl&eacute; fut parti, Corneille appela deux de ses serviteurs, et un soldat pieux d&#39;entre ceux qui &eacute;taient attach&eacute;s &agrave; sa personne;</p>

<p><sup class="versenum">8&nbsp;</sup>et, apr&egrave;s leur avoir tout racont&eacute;, il les envoya &agrave; Jopp&eacute;.</p>

<p><sup class="versenum">9&nbsp;</sup>Le lendemain, comme ils &eacute;taient en route, et qu&#39;ils approchaient de la ville, Pierre monta sur le toit, vers la sixi&egrave;me heure, pour prier.</p>

<p><sup class="versenum">10&nbsp;</sup>Il eut faim, et il voulut manger. Pendant qu&#39;on lui pr&eacute;parait &agrave; manger, il tomba en extase.</p>

<p><sup class="versenum">11&nbsp;</sup>Il vit le ciel ouvert, et un objet semblable &agrave; une grande nappe attach&eacute;e par les quatre coins, qui descendait et s&#39;abaissait vers la terre,</p>

<p><sup class="versenum">12&nbsp;</sup>et o&ugrave; se trouvaient tous les quadrup&egrave;des et les reptiles de la terre et les oiseaux du ciel.</p>

<p><sup class="versenum">13&nbsp;</sup>Et une voix lui dit: L&egrave;ve-toi, Pierre, tue et mange.</p>

<p><sup class="versenum">14&nbsp;</sup>Mais Pierre dit: Non, Seigneur, car je n&#39;ai jamais rien mang&eacute; de souill&eacute; ni d&#39;impur.</p>

<p><sup class="versenum">15&nbsp;</sup>Et pour la seconde fois la voix se fit encore entendre &agrave; lui: Ce que Dieu a d&eacute;clar&eacute; pur, ne le regarde pas comme souill&eacute;.</p>

<p><sup class="versenum">16&nbsp;</sup>Cela arriva jusqu&#39;&agrave; trois fois; et aussit&ocirc;t apr&egrave;s, l&#39;objet fut retir&eacute; dans le ciel.</p>

<p><sup class="versenum">17&nbsp;</sup>Tandis que Pierre ne savait en lui-m&ecirc;me que penser du sens de la vision qu&#39;il avait eue, voici, les hommes envoy&eacute;s par Corneille, s&#39;&eacute;tant inform&eacute;s de la maison de Simon, se pr&eacute;sent&egrave;rent &agrave; la porte,</p>

<p><sup class="versenum">18&nbsp;</sup>et demand&egrave;rent &agrave; haute voix si c&#39;&eacute;tait l&agrave; que logeait Simon, surnomm&eacute; Pierre.</p>

<p><sup class="versenum">19&nbsp;</sup>Et comme Pierre &eacute;tait &agrave; r&eacute;fl&eacute;chir sur la vision, l&#39;Esprit lui dit: Voici, trois hommes te demandent;</p>

<p><sup class="versenum">20&nbsp;</sup>l&egrave;ve-toi, descends, et pars avec eux sans h&eacute;siter, car c&#39;est moi qui les ai envoy&eacute;s.</p>

<p><sup class="versenum">21&nbsp;</sup>Pierre donc descendit, et il dit &agrave; ces hommes: Voici, je suis celui que vous cherchez; quel est le motif qui vous am&egrave;ne?</p>

<p><sup class="versenum">22&nbsp;</sup>Ils r&eacute;pondirent: Corneille, centenier, homme juste et craignant Dieu, et de qui toute la nation des Juifs rend un bon t&eacute;moignage, a &eacute;t&eacute; divinement averti par un saint ange de te faire venir dans sa maison et d&#39;entendre tes paroles.</p>

<p><sup class="versenum">23&nbsp;</sup>Pierre donc les fit entrer, et les logea. Le lendemain, il se leva, et partit avec eux. Quelques-uns des fr&egrave;res de Jopp&eacute; l&#39;accompagn&egrave;rent.</p>

<p><sup class="versenum">24&nbsp;</sup>Ils arriv&egrave;rent &agrave; C&eacute;sar&eacute;e le jour suivant. Corneille les attendait, et avait invit&eacute; ses parents et ses amis intimes.</p>

<p><sup class="versenum">25&nbsp;</sup>Lorsque Pierre entra, Corneille, qui &eacute;tait all&eacute; au-devant de lui, tomba &agrave; ses pieds et se prosterna.</p>

<p><sup class="versenum">26&nbsp;</sup>Mais Pierre le releva, en disant: L&egrave;ve-toi; moi aussi, je suis un homme.</p>

<p><sup class="versenum">27&nbsp;</sup>Et conversant avec lui, il entra, et trouva beaucoup de personnes r&eacute;unies.</p>

<p><sup class="versenum">28&nbsp;</sup>Vous savez, leur dit-il, qu&#39;il est d&eacute;fendu &agrave; un Juif de se lier avec un &eacute;tranger ou d&#39;entrer chez lui; mais Dieu m&#39;a appris &agrave; ne regarder aucun homme comme souill&eacute; et impur.</p>

<p><sup class="versenum">29&nbsp;</sup>C&#39;est pourquoi je n&#39;ai pas eu d&#39;objection &agrave; venir, puisque vous m&#39;avez appel&eacute;; je vous demande donc pour quel motif vous m&#39;avez envoy&eacute; chercher.</p>

<p><sup class="versenum">30&nbsp;</sup>Corneille dit: Il y a quatre jours, &agrave; cette heure-ci, je priais dans ma maison &agrave; la neuvi&egrave;me heure; et voici, un homme v&ecirc;tu d&#39;un habit &eacute;clatant se pr&eacute;senta devant moi, et dit:</p>

<p><sup class="versenum">31&nbsp;</sup>Corneille, ta pri&egrave;re a &eacute;t&eacute; exauc&eacute;e, et Dieu s&#39;est souvenu de tes aum&ocirc;nes.</p>

<p><sup class="versenum">32&nbsp;</sup>Envoie donc &agrave; Jopp&eacute;, et fais venir Simon, surnomm&eacute; Pierre; il est log&eacute; dans la maison de Simon, corroyeur, pr&egrave;s de la mer.</p>

<p><sup class="versenum">33&nbsp;</sup>Aussit&ocirc;t j&#39;ai envoy&eacute; vers toi, et tu as bien fait de venir. Maintenant donc nous sommes tous devant Dieu, pour entendre tout ce que le Seigneur t&#39;a ordonn&eacute; de nous dire.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/319.mp4" type="button" class="external-movie">
         Regardez Actes 10:1-33 </button>
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

<p>Il s&rsquo;agissait d&rsquo;un voyage de 2-jours de Jopp&eacute; &agrave; C&eacute;sar&eacute;e. &Aacute; travers une s&eacute;rie de vision, J&eacute;sus aide Pierre et les croyants juifs qui sont avec lui &agrave; franchir une barri&egrave;re culturelle dans l&rsquo;&eacute;glise Juive. Il &eacute;tait interdit &agrave; un bon praticien Juif d&rsquo;entrer dans la maison d&rsquo;un pa&iuml;en. J&eacute;sus envoie encore Pierre dans la maison de Corneille. Non seulement Corneille &eacute;tait un pa&iuml;en mais aussi un centenier de l&rsquo;Empire Romain &ndash; un officier charg&eacute; d&rsquo;environ 80-100 soldats du r&eacute;giment italien. Corneille est un bon exemple d&rsquo;une personne de paix. C&rsquo;est quelqu&rsquo;un qu&rsquo;on n&rsquo;esp&eacute;rait pas et dont le c&oelig;ur a &eacute;t&eacute; dispos&eacute; par J&eacute;sus, et qui rassemble d&rsquo;autres personnes de son r&eacute;seau relationnel pour &eacute;couter avec lui au sujet de J&eacute;sus. Cette histoire montre &nbsp;comment le Seigneur dispose le c&oelig;ur d&rsquo;un messager et celui d&rsquo;une personne de paix.</p>

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

			<td class="social" @click="share('lesson', 'Jésus prépare les c\'urs: ', '/content/M2/fra/multiply3/mutiply319.html')">
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