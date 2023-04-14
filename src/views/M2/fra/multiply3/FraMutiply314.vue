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
                        <div class="chapter_number ltr"><h1>14.</h1></div>
                        <div class="chapter_title ltr"><h1>Philippe fait des disciples et implante une église à Samarie</h1></div>
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
	<li>Lisez ou observez Actes 8:4-25 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 8:4-25</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">4&nbsp;</sup>Ceux qui avaient &eacute;t&eacute; dispers&eacute;s allaient de lieu en lieu, annon&ccedil;ant la bonne nouvelle de la parole.</p>

<p><sup class="versenum">5&nbsp;</sup>Philippe, &eacute;tant descendu dans la ville de Samarie, y pr&ecirc;cha le Christ.</p>

<p><sup class="versenum">6&nbsp;</sup>Les foules tout enti&egrave;res &eacute;taient attentives &agrave; ce que disait Philippe, lorsqu&#39;elles apprirent et virent les miracles qu&#39;il faisait.</p>

<p><sup class="versenum">7&nbsp;</sup>Car des esprits impurs sortirent de plusieurs d&eacute;moniaques, en poussant de grands cris, et beaucoup de paralytiques et de boiteux furent gu&eacute;ris.</p>

<p><sup class="versenum">8&nbsp;</sup>Et il y eut une grande joie dans cette ville.</p>

<p><sup class="versenum">9&nbsp;</sup>Il y avait auparavant dans la ville un homme nomm&eacute; Simon, qui, se donnant pour un personnage important, exer&ccedil;ait la magie et provoquait l&#39;&eacute;tonnement du peuple de la Samarie.</p>

<p><sup class="versenum">10&nbsp;</sup>Tous, depuis le plus petit jusqu&#39;au plus grand, l&#39;&eacute;coutaient attentivement, et disaient: Celui-ci est la puissance de Dieu, celle qui s&#39;appelle la grande.</p>

<p><sup class="versenum">11&nbsp;</sup>Ils l&#39;&eacute;coutaient attentivement, parce qu&#39;il les avait longtemps &eacute;tonn&eacute;s par ses actes de magie.</p>

<p><sup class="versenum">12&nbsp;</sup>Mais, quand ils eurent cru &agrave; Philippe, qui leur annon&ccedil;ait la bonne nouvelle du royaume de Dieu et du nom de J&eacute;sus Christ, hommes et femmes se firent baptiser.</p>

<p><sup class="versenum">13&nbsp;</sup>Simon lui-m&ecirc;me crut, et, apr&egrave;s avoir &eacute;t&eacute; baptis&eacute;, il ne quittait plus Philippe, et il voyait avec &eacute;tonnement les miracles et les grands prodiges qui s&#39;op&eacute;raient.</p>

<p><sup class="versenum">14&nbsp;</sup>Les ap&ocirc;tres, qui &eacute;taient &agrave; J&eacute;rusalem, ayant appris que la Samarie avait re&ccedil;u la parole de Dieu, y envoy&egrave;rent Pierre et Jean.</p>

<p><sup class="versenum">15&nbsp;</sup>Ceux-ci, arriv&eacute;s chez les Samaritains, pri&egrave;rent pour eux, afin qu&#39;ils re&ccedil;ussent le Saint Esprit.</p>

<p><sup class="versenum">16&nbsp;</sup>Car il n&#39;&eacute;tait encore descendu sur aucun d&#39;eux; ils avaient seulement &eacute;t&eacute; baptis&eacute;s au nom du Seigneur J&eacute;sus.</p>

<p><sup class="versenum">17&nbsp;</sup>Alors Pierre et Jean leur impos&egrave;rent les mains, et ils re&ccedil;urent le Saint Esprit.</p>

<p><sup class="versenum">18&nbsp;</sup>Lorsque Simon vit que le Saint Esprit &eacute;tait donn&eacute; par l&#39;imposition des mains des ap&ocirc;tres, il leur offrit de l&#39;argent,</p>

<p><sup class="versenum">19&nbsp;</sup>en disant: Accordez-moi aussi ce pouvoir, afin que celui &agrave; qui j&#39;imposerai les mains re&ccedil;oive le Saint Esprit.</p>

<p><sup class="versenum">20&nbsp;</sup>Mais Pierre lui dit: Que ton argent p&eacute;risse avec toi, puisque tu as cru que le don de Dieu s&#39;acqu&eacute;rait &agrave; prix d&#39;argent!</p>

<p><sup class="versenum">21&nbsp;</sup>Il n&#39;y a pour toi ni part ni lot dans cette affaire, car ton coeur n&#39;est pas droit devant Dieu.</p>

<p><sup class="versenum">22&nbsp;</sup>Repens-toi donc de ta m&eacute;chancet&eacute;, et prie le Seigneur pour que la pens&eacute;e de ton coeur te soit pardonn&eacute;e, s&#39;il est possible;</p>

<p><sup class="versenum">23&nbsp;</sup>car je vois que tu es dans un fiel amer et dans les liens de l&#39;iniquit&eacute;.</p>

<p><sup class="versenum">24&nbsp;</sup>Simon r&eacute;pondit: Priez vous-m&ecirc;mes le Seigneur pour moi, afin qu&#39;il ne m&#39;arrive rien de ce que vous avez dit.</p>

<p><sup class="versenum">25&nbsp;</sup>Apr&egrave;s avoir rendu t&eacute;moignage &agrave; la parole du Seigneur, et apr&egrave;s l&#39;avoir pr&ecirc;ch&eacute;e, Pierre et Jean retourn&egrave;rent &agrave; J&eacute;rusalem, en annon&ccedil;ant la bonne nouvelle dans plusieurs villages des Samaritains.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/314.mp4" type="button" class="external-movie">
         Regardez Actes 8:4-25 </button>
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

<p>Samarie &eacute;tait le nom d&rsquo;une grande r&eacute;gion de la Palestine dans le nord de J&eacute;rusalem. Comme &Eacute;tienne, Philippe &eacute;tait un de ces sept choisit &nbsp;pour aider &agrave; prendre soin des veuves de J&eacute;rusalem. Nous voyons tr&egrave;s t&ocirc;t l&rsquo;efficacit&eacute; du discipolat en faisant les m&ecirc;mes choses que les Ap&ocirc;tres ont eu &agrave; faire. Philippe a gu&eacute;ri beaucoup de personnes, a chass&eacute; les d&eacute;mons et a pr&ecirc;ch&eacute; sur le Royaume. C&rsquo;est la premi&egrave;re fois dans le livre des Actes que l&rsquo;&Eacute;vangile franchit les barri&egrave;res pour atteindre la culture des non-juifs, ainsi Pierre et Jean &nbsp;ont &eacute;t&eacute; envoy&eacute;s pour approuver le travail effectu&eacute;. Le Seigneur a utilis&eacute; cette exp&eacute;rience pour confirmer &agrave; Pierre et Jean que l&rsquo;&eacute;vangile &eacute;tait pour tout le monde. Pierre et Jean ont &eacute;t&eacute; donc encourag&eacute;s par ce que le Seigneur avait fait. Ils ont commenc&eacute; de nouvelles communaut&eacute;s de nouveaux croyants dans d&rsquo;autres villages Samaritains pendant leur retour de voyage &agrave; J&eacute;rusalem. Nous apprenons que la mort d&rsquo;&Eacute;tienne et la pers&eacute;cution qui a suivi, ont contribu&eacute;es ensemble selon le plan de Dieu &agrave; r&eacute;pandre Son royaume et b&acirc;tir Son &eacute;glise.</p>

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

			<td class="social" @click="share('lesson', 'Philippe fait des disciples et implante une église à Samarie: ', '/content/M2/fra/multiply3/mutiply314.html')">
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