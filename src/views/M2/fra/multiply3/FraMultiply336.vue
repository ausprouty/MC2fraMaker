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
                        <div class="chapter_number ltr"><h1>36.</h1></div>
                        <div class="chapter_title ltr"><h1>Implantation d'église dans la capitale de l'Achaïe  (Corinthe)</h1></div>
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
	<li>Lisez ou observez Actes 18:1-22 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 18:1-22</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Apr&egrave;s cela, Paul partit d&#39;Ath&egrave;nes, et se rendit &agrave; Corinthe.</p>

<p><sup class="versenum">2&nbsp;</sup>Il y trouva un Juif nomm&eacute; Aquilas, originaire du Pont, r&eacute;cemment arriv&eacute; d&#39;Italie avec sa femme Priscille, parce que Claude avait ordonn&eacute; &agrave; tous les Juifs de sortir de Rome. Il se lia avec eux;</p>

<p><sup class="versenum">3&nbsp;</sup>et, comme il avait le m&ecirc;me m&eacute;tier, il demeura chez eux et y travailla: ils &eacute;taient faiseurs de tentes.</p>

<p><sup class="versenum">4&nbsp;</sup>Paul discourait dans la synagogue chaque sabbat, et il persuadait des Juifs et des Grecs.</p>

<p><sup class="versenum">5&nbsp;</sup>Mais quand Silas et Timoth&eacute;e furent arriv&eacute;s de la Mac&eacute;doine, il se donna tout entier &agrave; la parole, attestant aux Juifs que J&eacute;sus &eacute;tait le Christ.</p>

<p><sup class="versenum">6&nbsp;</sup>Les Juifs faisant alors de l&#39;opposition et se livrant &agrave; des injures, Paul secoua ses v&ecirc;tements, et leur dit: Que votre sang retombe sur votre t&ecirc;te! J&#39;en suis pur. D&egrave;s maintenant, j&#39;irai vers les pa&iuml;ens.</p>

<p><sup class="versenum">7&nbsp;</sup>Et sortant de l&agrave;, il entra chez un nomm&eacute; Justus, homme craignant Dieu, et dont la maison &eacute;tait contigu&euml; &agrave; la synagogue.</p>

<p><sup class="versenum">8&nbsp;</sup>Cependant Crispus, le chef de la synagogue, crut au Seigneur avec toute sa famille. Et plusieurs Corinthiens, qui avaient entendu Paul, crurent aussi, et furent baptis&eacute;s.</p>

<p><sup class="versenum">9&nbsp;</sup>Le Seigneur dit &agrave; Paul en vision pendant la nuit: Ne crains point; mais parle, et ne te tais point,</p>

<p><sup class="versenum">10&nbsp;</sup>Car je suis avec toi, et personne ne mettra la main sur toi pour te faire du mal: parle, car j&#39;ai un peuple nombreux dans cette ville.</p>

<p><sup class="versenum">11&nbsp;</sup>Il y demeura un an et six mois, enseignant parmi les Corinthiens la parole de Dieu.</p>

<p><sup class="versenum">12&nbsp;</sup>Du temps que Gallion &eacute;tait proconsul de l&#39;Acha&iuml;e, les Juifs se soulev&egrave;rent unanimement contre Paul, et le men&egrave;rent devant le tribunal,</p>

<p><sup class="versenum">13&nbsp;</sup>en disant: Cet homme excite les gens &agrave; servir Dieu d&#39;une mani&egrave;re contraire &agrave; la loi.</p>

<p><sup class="versenum">14&nbsp;</sup>Paul allait ouvrir la bouche, lorsque Gallion dit aux Juifs: S&#39;il s&#39;agissait de quelque injustice ou de quelque m&eacute;chante action, je vous &eacute;couterais comme de raison, &ocirc; Juifs;</p>

<p><sup class="versenum">15&nbsp;</sup>mais, s&#39;il s&#39;agit de discussions sur une parole, sur des noms, et sur votre loi, cela vous regarde: je ne veux pas &ecirc;tre juge de ces choses.</p>

<p><sup class="versenum">16&nbsp;</sup>Et il les renvoya du tribunal.</p>

<p><sup class="versenum">17&nbsp;</sup>Alors tous, se saisissant de Sosth&egrave;ne, le chef de la synagogue, le battirent devant le tribunal, sans que Gallion s&#39;en m&icirc;t en peine.</p>

<p><sup class="versenum">18&nbsp;</sup>Paul resta encore assez longtemps &agrave; Corinthe. Ensuite il prit cong&eacute; des fr&egrave;res, et s&#39;embarqua pour la Syrie, avec Priscille et Aquilas, apr&egrave;s s&#39;&ecirc;tre fait raser la t&ecirc;te &agrave; Cenchr&eacute;es, car il avait fait un voeu.</p>

<p><sup class="versenum">19&nbsp;</sup>Ils arriv&egrave;rent &agrave; &Eacute;ph&egrave;se, et Paul y laissa ses compagnons. &Eacute;tant entr&eacute; dans la synagogue, il s&#39;entretint avec les Juifs,</p>

<p><sup class="versenum">20&nbsp;</sup>qui le pri&egrave;rent de prolonger son s&eacute;jour.</p>

<p><sup class="versenum">21&nbsp;</sup>Mais il n&#39;y consentit point, et il prit cong&eacute; d&#39;eux, en disant: Il faut absolument que je c&eacute;l&egrave;bre la f&ecirc;te prochaine &agrave; J&eacute;rusalem. Je reviendrai vers vous, si Dieu le veut. Et il partit d&#39;&Eacute;ph&egrave;se.</p>

<p><sup class="versenum">22&nbsp;</sup>&Eacute;tant d&eacute;barqu&eacute; &agrave; C&eacute;sar&eacute;e, il monta &agrave; J&eacute;rusalem, et, apr&egrave;s avoir salu&eacute; l&#39;&Eacute;glise, il descendit &agrave; Antioche.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/336.mp4" type="button" class="external-movie">
         Regardez Actes 18:1-22 </button>
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
	<li class="nobreak-final-final">Corinthe &eacute;tait une importante ville &eacute;conomique dans l&rsquo;ancien monde et connu pour sa culture d&rsquo;immoralit&eacute;. Lorsque Paul arriva, il rencontra Aquilas et Priscille qui venaient de rentrer de Rome. Ils avaient le m&ecirc;me m&eacute;tier que Paul. Leur &eacute;quipe de mari-femme est devenue une puissante &eacute;quipe d&rsquo;implantation d&rsquo;&eacute;glises. Paul a travaill&eacute; avec eux dans le domaine de leur m&eacute;tier et dans le minist&egrave;re. Lorsque Silas et Timoth&eacute;e sont revenus de Mac&eacute;doine, ils ont apport&eacute; de soutien financier et les nouvelles des nouveaux croyants de Thessalonique (<span class="popup-link" @click = "popUp('pop3')"> 1 Thessaloniciens 3:2</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">2&nbsp;</sup>nous envoy&acirc;mes Timoth&eacute;e, notre fr&egrave;re, ministre de Dieu dans l&#39;&Eacute;vangile de Christ, pour vous affermir et vous exhorter au sujet de votre foi,</p>
	<!-- end bible --></div>
	Paul a &eacute;crit ses deux lettres adress&eacute;es aux chr&eacute;tiens de Thessalonique pendant qu&rsquo;il implantait des &eacute;glises &agrave; Corinthe. Paul a eu beaucoup de pressions sociales et a combattu la peur (<span class="popup-link" @click = "popUp('pop4')"> Actes 18:9</span>),&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">9&nbsp;</sup>Le Seigneur dit &agrave; Paul en vision pendant la nuit: Ne crains point; mais parle, et ne te tais point,</p>
	<!-- end bible --></div>
	&nbsp;mais le Seigneur lui a dit de continuer.<br><br>Lisez <span class="popup-link" @click = "popUp('pop5')"> 1 Corinthiens 1:14-16</span>.&nbsp;
	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">14&nbsp;</sup>Je rends gr&acirc;ces &agrave; Dieu de ce que je n&#39;ai baptis&eacute; aucun de vous, except&eacute; Crispus et Ga&iuml;us,</p>

	<p><sup class="versenum">15&nbsp;</sup>afin que personne ne dise que vous avez &eacute;t&eacute; baptis&eacute;s en mon nom.</p>

	<p><sup class="versenum">16&nbsp;</sup>J&#39;ai encore baptis&eacute; la famille de St&eacute;phanas; du reste, je ne sache pas que j&#39;aie baptis&eacute; quelque autre personne.</p>
	<!-- end bible --></div>
	Un grand nombre de personnes a cru en J&eacute;sus, cependant, dans la lettre de Paul aux Corinthiens, nous voyons que Paul a seulement baptis&eacute; les premiers croyants. Nous apprenons l&rsquo;importance d&rsquo;autonomiser les nouveaux croyants en vue de la mission qui consiste &agrave; faire des disciples, en les baptisant et en les enseignant simplement comme le recommande J&eacute;sus.</li>
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

			<td class="social" @click="share('lesson', 'Implantation d\'église dans la capitale de l\'Achaïe  (Corinthe): ', '/content/M2/fra/multiply3/multiply336.html')">
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