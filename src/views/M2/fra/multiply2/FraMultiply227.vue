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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply2-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>27.</h1></div>
                        <div class="chapter_title ltr"><h1>Les Attentes du Leadership</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</p>

</div>

<h2>Soin</h2>

<p>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la Fid&eacute;lit&eacute;</h2>

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Luc 6:20-26 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 6:20-26</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">20&nbsp;</sup>Alors J&eacute;sus, levant les yeux sur ses disciples, dit: Heureux vous qui &ecirc;tes pauvres, car le royaume de Dieu est &agrave; vous!</p>

<p><sup class="versenum">21&nbsp;</sup>Heureux vous qui avez faim maintenant, car vous serez rassasi&eacute;s! Heureux vous qui pleurez maintenant, car vous serez dans la joie!</p>

<p><sup class="versenum">22&nbsp;</sup>Heureux serez-vous, lorsque les hommes vous ha&iuml;ront, lorsqu&#39;on vous chassera, vous outragera, et qu&#39;on rejettera votre nom comme inf&acirc;me, &agrave; cause du Fils de l&#39;homme!</p>

<p><sup class="versenum">23&nbsp;</sup>R&eacute;jouissez-vous en ce jour-l&agrave; et tressaillez d&#39;all&eacute;gresse, parce que votre r&eacute;compense sera grande dans le ciel; car c&#39;est ainsi que leurs p&egrave;res traitaient les proph&egrave;tes.</p>

<p><sup class="versenum">24&nbsp;</sup>Mais, malheur &agrave; vous, riches, car vous avez votre consolation!</p>

<p><sup class="versenum">25&nbsp;</sup>Malheur &agrave; vous qui &ecirc;tes rassasi&eacute;s, car vous aurez faim! Malheur &agrave; vous qui riez maintenant, car vous serez dans le deuil et dans les larmes!</p>

<p><sup class="versenum">26&nbsp;</sup>Malheur, lorsque tous les hommes diront du bien de vous, car c&#39;est ainsi qu&#39;agissaient leurs p&egrave;res &agrave; l&#39;&eacute;gard des faux proph&egrave;tes!</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/227.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 6:20-26&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<p>Etudiez chaque passage en utilisant les questions de discussion suivantes:</p>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ?</li>
	<li>Qu&rsquo;est ce qui est nouveau ou s&rsquo;est d&eacute;velopp&eacute; &agrave; ce point de l&rsquo;histoire de J&eacute;sus?</li>
	<li>Quelle implication du point de vue de l&rsquo;humanit&eacute; ou de la divinit&eacute; de J&eacute;sus voyez-vous dans ce passage ?</li>
</ul>

<p>Questions suppl&eacute;mentaires que vous pouvez poser:</p>

<ul>
	<li>Qu&rsquo;est-ce que ses disciples apprennent?</li>
	<li>Qu&rsquo;est-ce que J&eacute;sus est en train de nous montrer au sujet de sa vie et de son minist&egrave;re (ou leadership) ?</li>
	<li>Qu&rsquo;est ce que J&eacute;sus est en train de montrer au sujet du leadership empreint de pi&eacute;t&eacute; ?</li>
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


<h2>Lire, raconter et corriger</h2>

<p>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</p>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p>Apr&egrave;s avoir d&eacute;sign&eacute; les 12 leaders, J&eacute;sus enseigne ensuite ses disciples sur les attentes du Royaume. Un principe cl&eacute; du leadership est d&#39;&eacute;noncer clairement les attentes. Qu&#39;est-ce qui caract&eacute;risera la vie dans le royaume et la communaut&eacute;? J&eacute;sus d&eacute;taille pour eux une liste de qualit&eacute;s en contraste frappant avec les attitudes de la soci&eacute;t&eacute; dans son ensemble mais descriptif de son propre exemple de vie. Le style de vie des dirigeants et de la communaut&eacute; du royaume construit autour de J&eacute;sus doit refl&eacute;ter son propre caract&egrave;re et ses priorit&eacute;s, pas ceux du monde.</p>

<p>Pour une &eacute;tude approfondie <span class="popup-link" @click = "popUp('pop1')"> Matthieu 5:1-12</span>.</p>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">1 </sup>Voyant la foule, J&eacute;sus monta sur la montagne; et, apr&egrave;s qu&#39;il se fut assis, ses disciples s&#39;approch&egrave;rent de lui.</p>

<p><sup class="versenum">2&nbsp;</sup>Puis, ayant ouvert la bouche, il les enseigna, et dit:</p>

<p><sup class="versenum">3&nbsp;</sup>Heureux les pauvres en esprit, car le royaume des cieux est &agrave; eux!</p>

<p><sup class="versenum">4&nbsp;</sup>Heureux les afflig&eacute;s, car ils seront consol&eacute;s!</p>

<p><sup class="versenum">5&nbsp;</sup>Heureux les d&eacute;bonnaires, car ils h&eacute;riteront la terre!</p>

<p><sup class="versenum">6&nbsp;</sup>Heureux ceux qui ont faim et soif de la justice, car ils seront rassasi&eacute;s!</p>

<p><sup class="versenum">7&nbsp;</sup>Heureux les mis&eacute;ricordieux, car ils obtiendront mis&eacute;ricorde!</p>

<p><sup class="versenum">8&nbsp;</sup>Heureux ceux qui ont le coeur pur, car ils verront Dieu!</p>

<p><sup class="versenum">9&nbsp;</sup>Heureux ceux qui procurent la paix, car ils seront appel&eacute;s fils de Dieu!</p>

<p><sup class="versenum">10&nbsp;</sup>Heureux ceux qui sont pers&eacute;cut&eacute;s pour la justice, car le royaume des cieux est &agrave; eux!</p>

<p><sup class="versenum">11&nbsp;</sup>Heureux serez-vous, lorsqu&#39;on vous outragera, qu&#39;on vous pers&eacute;cutera et qu&#39;on dira faussement de vous toute sorte de mal, &agrave; cause de moi.</p>

<p><sup class="versenum">12&nbsp;</sup>R&eacute;jouissez-vous et soyez dans l&#39;all&eacute;gresse, parce que votre r&eacute;compense sera grande dans les cieux; car c&#39;est ainsi qu&#39;on a pers&eacute;cut&eacute; les proph&egrave;tes qui ont &eacute;t&eacute; avant vous.</p>
<!-- end bible --></div>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ Se Pr&eacute;parer pour la Mission</h2></div>
<div class="collapsed" id ="Text3">
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

<h2>Aller en Mission</h2>

<ul>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau envers qui vous prendrez l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>&Eacute;crivez les promesses &laquo; je le ferai d&rsquo;ici quand &raquo; et parlez-en &agrave; votre groupe.</li>
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


<h2>Prier pour la Mission</h2>

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</p>

<p>&nbsp;</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Les Attentes du Leadership: ', '/content/M2/fra/multiply2/multiply227.html')">
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