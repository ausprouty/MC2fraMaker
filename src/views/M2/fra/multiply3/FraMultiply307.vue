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
                        <div class="chapter_number ltr"><h1>7.</h1></div>
                        <div class="chapter_title ltr"><h1>Le courage face à la persécution</h1></div>
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
	<li>Lisez ou observez Actes 4:1-31 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 4:1-31</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Tandis que Pierre et Jean parlaient au peuple, survinrent les sacrificateurs, le commandant du temple, et les sadduc&eacute;ens,</p>

<p><sup class="versenum">2&nbsp;</sup>m&eacute;contents de ce qu&#39;ils enseignaient le peuple, et annon&ccedil;aient en la personne de J&eacute;sus la r&eacute;surrection des morts.</p>

<p><sup class="versenum">3&nbsp;</sup>Ils mirent les mains sur eux, et ils les jet&egrave;rent en prison jusqu&#39;au lendemain; car c&#39;&eacute;tait d&eacute;j&agrave; le soir.</p>

<p><sup class="versenum">4&nbsp;</sup>Cependant, beaucoup de ceux qui avaient entendu la parole crurent, et le nombre des hommes s&#39;&eacute;leva &agrave; environ cinq mille.</p>

<p><sup class="versenum">5&nbsp;</sup>Le lendemain, les chefs du peuple, les anciens et les scribes, s&#39;assembl&egrave;rent &agrave; J&eacute;rusalem,</p>

<p><sup class="versenum">6&nbsp;</sup>avec Anne, le souverain sacrificateur, Ca&iuml;phe, Jean, Alexandre, et tous ceux qui &eacute;taient de la race des principaux sacrificateurs.</p>

<p><sup class="versenum">7&nbsp;</sup>Ils firent placer au milieu d&#39;eux Pierre et Jean, et leur demand&egrave;rent: Par quel pouvoir, ou au nom de qui avez-vous fait cela?</p>

<p><sup class="versenum">8&nbsp;</sup>Alors Pierre, rempli du Saint Esprit, leur dit: Chefs du peuple, et anciens d&#39;Isra&euml;l,</p>

<p><sup class="versenum">9&nbsp;</sup>puisque nous sommes interrog&eacute;s aujourd&#39;hui sur un bienfait accord&eacute; &agrave; un homme malade, afin que nous disions comment il a &eacute;t&eacute; gu&eacute;ri,</p>

<p><sup class="versenum">10&nbsp;</sup>sachez-le tous, et que tout le peuple d&#39;Isra&euml;l le sache! C&#39;est par le nom de J&eacute;sus Christ de Nazareth, que vous avez &eacute;t&eacute; crucifi&eacute;, et que Dieu a ressuscit&eacute; des morts, c&#39;est par lui que cet homme se pr&eacute;sente en pleine sant&eacute; devant vous.</p>

<p><sup class="versenum">11&nbsp;</sup>J&eacute;sus est La pierre rejet&eacute;e par vous qui b&acirc;tissez, Et qui est devenue la principale de l&#39;angle.</p>

<p><sup class="versenum">12&nbsp;</sup>Il n&#39;y a de salut en aucun autre; car il n&#39;y a sous le ciel aucun autre nom qui ait &eacute;t&eacute; donn&eacute; parmi les hommes, par lequel nous devions &ecirc;tre sauv&eacute;s.</p>

<p><sup class="versenum">13&nbsp;</sup>Lorsqu&#39;ils virent l&#39;assurance de Pierre et de Jean, ils furent &eacute;tonn&eacute;s, sachant que c&#39;&eacute;taient des hommes du peuple sans instruction; et ils les reconnurent pour avoir &eacute;t&eacute; avec J&eacute;sus.</p>

<p><sup class="versenum">14&nbsp;</sup>Mais comme ils voyaient l&agrave; pr&egrave;s d&#39;eux l&#39;homme qui avait &eacute;t&eacute; gu&eacute;ri, ils n&#39;avaient rien &agrave; r&eacute;pliquer.</p>

<p><sup class="versenum">15&nbsp;</sup>Ils leur ordonn&egrave;rent de sortir du sanh&eacute;drin, et ils d&eacute;lib&eacute;r&egrave;rent entre eux, disant: Que ferons-nous &agrave; ces hommes?</p>

<p><sup class="versenum">16&nbsp;</sup>Car il est manifeste pour tous les habitants de J&eacute;rusalem qu&#39;un miracle signal&eacute; a &eacute;t&eacute; accompli par eux, et nous ne pouvons pas le nier.</p>

<p><sup class="versenum">17&nbsp;</sup>Mais, afin que la chose ne se r&eacute;pande pas davantage parmi le peuple, d&eacute;fendons-leur avec menaces de parler d&eacute;sormais &agrave; qui que ce soit en ce nom-l&agrave;.</p>

<p><sup class="versenum">18&nbsp;</sup>Et les ayant appel&eacute;s, ils leur d&eacute;fendirent absolument de parler et d&#39;enseigner au nom de J&eacute;sus.</p>

<p><sup class="versenum">19&nbsp;</sup>Pierre et Jean leur r&eacute;pondirent: Jugez s&#39;il est juste, devant Dieu, de vous ob&eacute;ir plut&ocirc;t qu&#39;&agrave; Dieu;</p>

<p><sup class="versenum">20&nbsp;</sup>car nous ne pouvons pas ne pas parler de ce que nous avons vu et entendu.</p>

<p><sup class="versenum">21&nbsp;</sup>Ils leur firent de nouvelles menaces, et les rel&acirc;ch&egrave;rent, ne sachant comment les punir, &agrave; cause du peuple, parce que tous glorifiaient Dieu de ce qui &eacute;tait arriv&eacute;.</p>

<p><sup class="versenum">22&nbsp;</sup>Car l&#39;homme qui avait &eacute;t&eacute; l&#39;objet de cette gu&eacute;rison miraculeuse &eacute;tait &acirc;g&eacute; de plus de quarante ans.</p>

<p><sup class="versenum">23&nbsp;</sup>Apr&egrave;s avoir &eacute;t&eacute; rel&acirc;ch&eacute;s, ils all&egrave;rent vers les leurs, et racont&egrave;rent tout ce que les principaux sacrificateurs et les anciens leur avaient dit.</p>

<p><sup class="versenum">24&nbsp;</sup>Lorsqu&#39;ils l&#39;eurent entendu, ils &eacute;lev&egrave;rent &agrave; Dieu la voix tous ensemble, et dirent: Seigneur, toi qui as fait le ciel, la terre, la mer, et tout ce qui s&#39;y trouve,</p>

<p><sup class="versenum">25&nbsp;</sup>c&#39;est toi qui as dit par le Saint Esprit, par la bouche de notre p&egrave;re, ton serviteur David: Pourquoi ce tumulte parmi les nations, Et ces vaines pens&eacute;es parmi les peuples?</p>

<p><sup class="versenum">26&nbsp;</sup>Les rois de la terre se sont soulev&eacute;s, Et les princes se sont ligu&eacute;s Contre le Seigneur et contre son Oint.</p>

<p><sup class="versenum">27&nbsp;</sup>En effet, contre ton saint serviteur J&eacute;sus, que tu as oint, H&eacute;rode et Ponce Pilate se sont ligu&eacute;s dans cette ville avec les nations et avec les peuples d&#39;Isra&euml;l,</p>

<p><sup class="versenum">28&nbsp;</sup>pour faire tout ce que ta main et ton conseil avaient arr&ecirc;t&eacute; d&#39;avance.</p>

<p><sup class="versenum">29&nbsp;</sup>Et maintenant, Seigneur, vois leurs menaces, et donne &agrave; tes serviteurs d&#39;annoncer ta parole avec une pleine assurance,</p>

<p><sup class="versenum">30&nbsp;</sup>en &eacute;tendant ta main, pour qu&#39;il se fasse des gu&eacute;risons, des miracles et des prodiges, par le nom de ton saint serviteur J&eacute;sus.</p>

<p><sup class="versenum">31&nbsp;</sup>Quand ils eurent pri&eacute;, le lieu o&ugrave; ils &eacute;taient assembl&eacute;s trembla; ils furent tous remplis du Saint Esprit, et ils annon&ccedil;aient la parole de Dieu avec assurance.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/307.mp4" type="button" class="external-movie">
         Regardez Actes 4:1-31 </button>
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
	<li class="nobreak-final-final"><span><span>Les chefs religieux &eacute;taient contrari&eacute;s du fait que Pierre enseigne aux gens la r&eacute;surrection des morts par J&eacute;sus&nbsp;; ils ont alors arr&ecirc;t&eacute; Pierre et Jean. Lorsque les foules ont assist&eacute; &agrave; la gu&eacute;rison du boiteux et ont &eacute;cout&eacute; le t&eacute;moignage de Pierre, 2 000 autres hommes, plus des femmes et des enfants, ont cru. J&eacute;sus avait enseign&eacute; aux ap&ocirc;tres de ne pas s&#39;inqui&eacute;ter de ce qu&#39;ils allaient dire lorsqu&#39;ils seraient men&eacute;s devant les autorit&eacute;s. Il a promis que l&#39;Esprit les conduira dans ce qu&#39;ils devaient dire (<span class="popup-link" @click = "popUp('pop3')"> Matthieu 10: 17-20</span>),</span></span>

	<div class="popup invisible" id="pop3"><span><span><!-- begin bible --> </span></span>

	<p><span><span><sup class="versenum">17&nbsp;</sup>Mettez-vous en garde contre les hommes; car ils vous livreront aux tribunaux, et ils vous battront de verges dans leurs synagogues;</span></span></p>
	<span><span> </span></span>

	<p><span><span><sup class="versenum">18&nbsp;</sup>vous serez men&eacute;s, &agrave; cause de moi, devant des gouverneurs et devant des rois, pour servir de t&eacute;moignage &agrave; eux et aux pa&iuml;ens.</span></span></p>
	<span><span> </span></span>

	<p><span><span><sup class="versenum">19&nbsp;</sup>Mais, quand on vous livrera, ne vous inqui&eacute;tez ni de la mani&egrave;re dont vous parlerez ni de ce que vous direz: ce que vous aurez &agrave; dire vous sera donn&eacute; &agrave; l&#39;heure m&ecirc;me;</span></span></p>
	<span><span> </span></span>

	<p><span><span><sup class="versenum">20&nbsp;</sup>car ce n&#39;est pas vous qui parlerez, c&#39;est l&#39;Esprit de votre P&egrave;re qui parlera en vous.</span></span></p>
	<span><span> <!-- end bible --> </span></span></div>
	<span><span>M&ecirc;me si Pierre et Jean n&#39;avaient pas re&ccedil;u une &eacute;ducation formelle, ils avaient un minist&egrave;re tr&egrave;s efficace, pour avoir appris de J&eacute;sus et &eacute;tant habilit&eacute;s par Son Esprit. Dans ce redoutable conflit avec les autorit&eacute;s, la riposte courageuse des croyants a &eacute;t&eacute; de prier pour avoir du courage face &agrave; la pers&eacute;cution afin qu&rsquo;ils puissent continuer &agrave; ob&eacute;ir &agrave; J&eacute;sus dans la mission.</span></span></li>
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

			<td class="social" @click="share('lesson', 'Le courage face à la persécution: ', '/content/M2/fra/multiply3/multiply307.html')">
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