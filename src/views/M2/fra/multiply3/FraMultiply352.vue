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
                        <div class="chapter_number ltr"><h1>52.</h1></div>
                        <div class="chapter_title ltr"><h1>La fidélité de Jésus à Sa promesse</h1></div>
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
	<li>Lisez ou observez Actes 27:27-44 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 27:27-44</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">27&nbsp;</sup>La quatorzi&egrave;me nuit, tandis que nous &eacute;tions ballott&eacute;s sur l&#39;Adriatique, les matelots, vers le milieu de la nuit, soup&ccedil;onn&egrave;rent qu&#39;on approchait de quelque terre.</p>

<p><sup class="versenum">28&nbsp;</sup>Ayant jet&eacute; la sonde, ils trouv&egrave;rent vingt brasses; un peu plus loin, ils la jet&egrave;rent de nouveau, et trouv&egrave;rent quinze brasses.</p>

<p><sup class="versenum">29&nbsp;</sup>Dans la crainte de heurter contre des &eacute;cueils, ils jet&egrave;rent quatre ancres de la poupe, et attendirent le jour avec impatience.</p>

<p><sup class="versenum">30&nbsp;</sup>Mais, comme les matelots cherchaient &agrave; s&#39;&eacute;chapper du navire, et mettaient la chaloupe &agrave; la mer sous pr&eacute;texte de jeter les ancres de la proue,</p>

<p><sup class="versenum">31&nbsp;</sup>Paul dit au centenier et aux soldats: Si ces hommes ne restent pas dans le navire, vous ne pouvez &ecirc;tre sauv&eacute;s.</p>

<p><sup class="versenum">32&nbsp;</sup>Alors les soldats coup&egrave;rent les cordes de la chaloupe, et la laiss&egrave;rent tomber.</p>

<p><sup class="versenum">33&nbsp;</sup>Avant que le jour par&ucirc;t, Paul exhorta tout le monde &agrave; prendre de la nourriture, disant: C&#39;est aujourd&#39;hui le quatorzi&egrave;me jour que vous &ecirc;tes dans l&#39;attente et que vous persistez &agrave; vous abstenir de manger.</p>

<p><sup class="versenum">34&nbsp;</sup>Je vous invite donc &agrave; prendre de la nourriture, car cela est n&eacute;cessaire pour votre salut, et il ne se perdra pas un cheveux de la t&ecirc;te d&#39;aucun de vous.</p>

<p><sup class="versenum">35&nbsp;</sup>Ayant ainsi parl&eacute;, il prit du pain, et, apr&egrave;s avoir rendu gr&acirc;ces &agrave; Dieu devant tous, il le rompit, et se mit &agrave; manger.</p>

<p><sup class="versenum">36&nbsp;</sup>Et tous, reprenant courage, mang&egrave;rent aussi.</p>

<p><sup class="versenum">37&nbsp;</sup>Nous &eacute;tions, dans le navire, deux cent soixante-seize personnes en tout.</p>

<p><sup class="versenum">38&nbsp;</sup>Quand ils eurent mang&eacute; suffisamment, ils all&eacute;g&egrave;rent le navire en jetant le bl&eacute; &agrave; la mer.</p>

<p><sup class="versenum">39&nbsp;</sup>Lorsque le jour fut venu, ils ne reconnurent point la terre; mais, ayant aper&ccedil;u un golfe avec une plage, ils r&eacute;solurent d&#39;y pousser le navire, s&#39;ils le pouvaient.</p>

<p><sup class="versenum">40&nbsp;</sup>Ils d&eacute;li&egrave;rent les ancres pour les laisser aller dans la mer, et ils rel&acirc;ch&egrave;rent en m&ecirc;me temps les attaches des gouvernails; puis ils mirent au vent la voile d&#39;artimon, et se dirig&egrave;rent vers le rivage.</p>

<p><sup class="versenum">41&nbsp;</sup>Mais ils rencontr&egrave;rent une langue de terre, o&ugrave; ils firent &eacute;chouer le navire; et la proue, s&#39;&eacute;tant engag&eacute;e, resta immobile, tandis que la poupe se brisait par la violence des vagues.</p>

<p><sup class="versenum">42&nbsp;</sup>Les soldats furent d&#39;avis de tuer les prisonniers, de peur que quelqu&#39;un d&#39;eux ne s&#39;&eacute;chapp&acirc;t &agrave; la nage.</p>

<p><sup class="versenum">43&nbsp;</sup>Mais le centenier, qui voulait sauver Paul, les emp&ecirc;cha d&#39;ex&eacute;cuter ce dessein. Il ordonna &agrave; ceux qui savaient nager de se jeter les premiers dans l&#39;eau pour gagner la terre,</p>

<p><sup class="versenum">44&nbsp;</sup>et aux autres de se mettre sur des planches ou sur des d&eacute;bris du navire. Et ainsi tous parvinrent &agrave; terre sains et saufs.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/352.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 27:27-44&nbsp; </button>
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

<p>La temp&ecirc;te a dur&eacute; plus de deux semaines &eacute;puisantes et terrifiantes! Paul a insist&eacute; sur le fait que les soldats devaient tous rester ensemble pour survivre. Ils ont fait face &agrave; un danger incroyable, mais J&eacute;sus a &eacute;t&eacute; fid&egrave;le &agrave; sa promesse et personne n&#39;a &eacute;t&eacute; bless&eacute;. Paul a montr&eacute; &agrave; ces non-croyants, la confiance en la fid&eacute;lit&eacute; et la bont&eacute; de Dieu et ils ont &eacute;t&eacute; encourag&eacute;s. C&#39;est un excellent exemple de valorisation de l&rsquo;intercession et de la prise en charge de toutes les personnes ind&eacute;pendamment de leur religion, race ou position, tout comme J&eacute;sus l&#39;a fait. Les gardes craignant qu&rsquo;ils ne s&rsquo;&eacute;chappent, voulaient ex&eacute;cuter tous les prisonniers, mais une fois de plus, Dieu a &oelig;uvr&eacute; &agrave; travers un centenier pour prot&eacute;ger Paul.</p>

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

			<td class="social" @click="share('lesson', 'La fidélité de Jésus à Sa promesse: ', '/content/M2/fra/multiply3/multiply352.html')">
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