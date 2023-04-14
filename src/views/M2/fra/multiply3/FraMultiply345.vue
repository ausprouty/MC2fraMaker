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
                        <div class="chapter_number ltr"><h1>45.</h1></div>
                        <div class="chapter_title ltr"><h1>La défense de Paul devant les Juifs</h1></div>
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
	<li>Lisez ou observez Actes 21:37-22:21 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 21:37-22:21</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">37&nbsp;</sup>Au moment d&#39;&ecirc;tre introduit dans la forteresse, Paul dit au tribun: M&#39;est-il permis de te dire quelque chose? Le tribun r&eacute;pondit: Tu sais le grec?</p>

<p><sup class="versenum">38&nbsp;</sup>Tu n&#39;es donc pas cet &Eacute;gyptien qui s&#39;est r&eacute;volt&eacute; derni&egrave;rement, et qui a emmen&eacute; dans le d&eacute;sert quatre mille brigands?</p>

<p><sup class="versenum">39&nbsp;</sup>Je suis Juif, reprit Paul, de Tarse en Cilicie, citoyen d&#39;une ville qui n&#39;est pas sans importance. Permets-moi, je te prie, de parler au peuple.</p>

<p><sup class="versenum">40&nbsp;</sup>Le tribun le lui ayant permis, Paul, debout sur les degr&eacute;s, fit signe de la main au peuple. Un profond silence s&#39;&eacute;tablit, et Paul, parlant en langue h&eacute;bra&iuml;que, dit:</p>

<p><sup class="versenum">1 </sup>Hommes fr&egrave;res et p&egrave;res, &eacute;coutez ce que j&#39;ai maintenant &agrave; vous dire pour ma d&eacute;fense!</p>

<p><sup class="versenum">2&nbsp;</sup>Lorsqu&#39;ils entendirent qu&#39;il leur parlait en langue h&eacute;bra&iuml;que, ils redoubl&egrave;rent de silence. Et Paul dit:</p>

<p><sup class="versenum">3&nbsp;</sup>je suis Juif, n&eacute; &agrave; Tarse en Cilicie; mais j&#39;ai &eacute;t&eacute; &eacute;lev&eacute; dans cette ville-ci, et instruit aux pieds de Gamaliel dans la connaissance exacte de la loi de nos p&egrave;res, &eacute;tant plein de z&egrave;le pour Dieu, comme vous l&#39;&ecirc;tes tous aujourd&#39;hui.</p>

<p><sup class="versenum">4&nbsp;</sup>J&#39;ai pers&eacute;cut&eacute; &agrave; mort cette doctrine, liant et mettant en prison hommes et femmes.</p>

<p><sup class="versenum">5&nbsp;</sup>Le souverain sacrificateur et tout le coll&egrave;ge des anciens m&#39;en sont t&eacute;moins. J&#39;ai m&ecirc;me re&ccedil;u d&#39;eux des lettres pour les fr&egrave;res de Damas, o&ugrave; je me rendis afin d&#39;amener li&eacute;s &agrave; J&eacute;rusalem ceux qui se trouvaient l&agrave; et de les faire punir.</p>

<p><sup class="versenum">6&nbsp;</sup>Comme j&#39;&eacute;tais en chemin, et que j&#39;approchais de Damas, tout &agrave; coup, vers midi, une grande lumi&egrave;re venant du ciel resplendit autour de moi.</p>

<p><sup class="versenum">7&nbsp;</sup>Je tombai par terre, et j&#39;entendis une voix qui me disait: Saul, Saul, pourquoi me pers&eacute;cutes-tu?</p>

<p><sup class="versenum">8&nbsp;</sup>Je r&eacute;pondis: Qui es-tu, Seigneur? Et il me dit: Je suis J&eacute;sus de Nazareth, que tu pers&eacute;cutes.</p>

<p><sup class="versenum">9&nbsp;</sup>Ceux qui &eacute;taient avec moi virent bien la lumi&egrave;re, mais ils n&#39;entendirent pas la voix de celui qui parlait. Alors je dis: Que ferai-je, Seigneur?</p>

<p><sup class="versenum">10&nbsp;</sup>Et le Seigneur me dit: L&egrave;ve-toi, va &agrave; Damas, et l&agrave; on te dira tout ce que tu dois faire.</p>

<p><sup class="versenum">11&nbsp;</sup>Comme je ne voyais rien, &agrave; cause de l&#39;&eacute;clat de cette lumi&egrave;re, ceux qui &eacute;taient avec moi me prirent par la main, et j&#39;arrivai &agrave; Damas.</p>

<p><sup class="versenum">12&nbsp;</sup>Or, un nomm&eacute; Ananias, homme pieux selon la loi, et de qui tous les Juifs demeurant &agrave; Damas rendaient un bon t&eacute;moignage, vint se pr&eacute;senter &agrave; moi,</p>

<p><sup class="versenum">13&nbsp;</sup>et me dit: Saul, mon fr&egrave;re, recouvre la vue. Au m&ecirc;me instant, je recouvrai la vue et je le regardai.</p>

<p><sup class="versenum">14&nbsp;</sup>Il dit: Le Dieu de nos p&egrave;res t&#39;a destin&eacute; &agrave; conna&icirc;tre sa volont&eacute;, &agrave; voir le Juste, et &agrave; entendre les paroles de sa bouche;</p>

<p><sup class="versenum">15&nbsp;</sup>car tu lui serviras de t&eacute;moin, aupr&egrave;s de tous les hommes, des choses que tu as vues et entendues.</p>

<p><sup class="versenum">16&nbsp;</sup>Et maintenant, que tardes-tu? L&egrave;ve-toi, sois baptis&eacute;, et lav&eacute; de tes p&eacute;ch&eacute;s, en invoquant le nom du Seigneur.</p>

<p><sup class="versenum">17&nbsp;</sup>De retour &agrave; J&eacute;rusalem, comme je priais dans le temple, je fus ravi en extase,</p>

<p><sup class="versenum">18&nbsp;</sup>et je vis le Seigneur qui me disait: H&acirc;te-toi, et sors promptement de J&eacute;rusalem, parce qu&#39;ils ne recevront pas ton t&eacute;moignage sur moi.</p>

<p><sup class="versenum">19&nbsp;</sup>Et je dis: Seigneur, ils savent eux-m&ecirc;mes que je faisais mettre en prison et battre de verges dans les synagogues ceux qui croyaient en toi, et que,</p>

<p><sup class="versenum">20&nbsp;</sup>lorsqu&#39;on r&eacute;pandit le sang d&#39;&Eacute;tienne, ton t&eacute;moin, j&#39;&eacute;tais moi-m&ecirc;me pr&eacute;sent, joignant mon approbation &agrave; celle des autres, et gardant les v&ecirc;tements de ceux qui le faisaient mourir.</p>

<p><sup class="versenum">21&nbsp;</sup>Alors il me dit: Va, je t&#39;enverrai au loin vers les nations...</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/345.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 21:37-22:21&nbsp; </button>
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
	<li class="nobreak-final-final">Le Seigneur avait pr&eacute;par&eacute; Paul pour ce moment &agrave; travers sa vie &agrave; Tarse, son &eacute;ducation grecque, sa formation d&#39;enseignant religieux juif et ses exp&eacute;riences missionnaires. C&#39;est la premi&egrave;re fois que Luc, l&#39;auteur des Actes, pr&eacute;sente Paul en train de pr&eacute;senter sa d&eacute;fense. Paul a dit &agrave; l&#39;&eacute;glise de Rome qu&#39;il n&#39;avait point honte de l&#39;&eacute;vangile (<span class="popup-link" @click = "popUp('pop3')"> Romains 1:16</span>),&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">16&nbsp;</sup>Car je n&#39;ai point honte de l&#39;&Eacute;vangile: c&#39;est une puissance de Dieu pour le salut de quiconque croit, du Juif premi&egrave;rement, puis du Grec,</p>
	<!-- end bible --></div>
	et il a continu&eacute; &agrave; partager l&#39;&eacute;vangile quelles que soient les circonstances ou les cons&eacute;quences. Paul profite de l&#39;occasion pour pr&eacute;senter &agrave; ses compatriotes le t&eacute;moignage sur: sa vie avant de rencontrer le J&eacute;sus vivant, comment il a rencontr&eacute; J&eacute;sus et comment J&eacute;sus a chang&eacute; sa vie et sa mission. Plus tard, Paul va encourager ses dirigeants de la prochaine g&eacute;n&eacute;ration, Timoth&eacute;e et Tite, &agrave; &ecirc;tre pr&ecirc;ts &agrave; chaque occasion pour partager leur exp&eacute;rience et leur connaissance de J&eacute;sus (<span class="popup-link" @click = "popUp('pop4')"> Tite 3: 1</span>;&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Rappelle-leur d&#39;&ecirc;tre soumis aux magistrats et aux autorit&eacute;s, d&#39;ob&eacute;ir, d&#39;&ecirc;tre pr&ecirc;ts &agrave; toute bonne oeuvre,</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop5')"> 2 Timoth&eacute;e 4: 2</span>).&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">2&nbsp;</sup>pr&ecirc;che la parole, insiste en toute occasion, favorable ou non, reprends, censure, exhorte, avec toute douceur et en instruisant.</p>
	<!-- end bible --></div>
	Par le t&eacute;moignage personnel de Paul, nous apprenons que les hommes et les femmes de l&rsquo;&Eacute;glise primitive ont souffert &agrave; cause de leur foi en J&eacute;sus (<span class="popup-link" @click = "popUp('pop6')"> Actes 22:4</span>).&nbsp;

	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>J&#39;ai pers&eacute;cut&eacute; &agrave; mort cette doctrine, liant et mettant en prison hommes et femmes.</p>
	<!-- end bible --></div>
	Les Juifs se sont constamment but&eacute;s contre le fait que Dieu accepterait tout le monde sans observer les pratiques religieuses juives.</li>
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

			<td class="social" @click="share('lesson', 'La défense de Paul devant les Juifs: ', '/content/M2/fra/multiply3/multiply345.html')">
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