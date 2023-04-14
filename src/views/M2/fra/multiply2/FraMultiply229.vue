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
                        <div class="chapter_number ltr"><h1>29.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership et  and Autorité</h1></div>
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
	<li>Lisez ou observez Luc 7:1-10 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 7:1-10</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Apr&egrave;s avoir achev&eacute; tous ces discours devant le peuple qui l&#39;&eacute;coutait, J&eacute;sus entra dans Caperna&uuml;m.</p>

<p><sup class="versenum">2&nbsp;</sup>Un centenier avait un serviteur auquel il &eacute;tait tr&egrave;s attach&eacute;, et qui se trouvait malade, sur le point de mourir.</p>

<p><sup class="versenum">3&nbsp;</sup>Ayant entendu parler de J&eacute;sus, il lui envoya quelques anciens des Juifs, pour le prier de venir gu&eacute;rir son serviteur.</p>

<p><sup class="versenum">4&nbsp;</sup>Ils arriv&egrave;rent aupr&egrave;s de J&eacute;sus, et lui adress&egrave;rent d&#39;instantes supplications, disant: Il m&eacute;rite que tu lui accordes cela;</p>

<p><sup class="versenum">5&nbsp;</sup>car il aime notre nation, et c&#39;est lui qui a b&acirc;ti notre synagogue.</p>

<p><sup class="versenum">6&nbsp;</sup>J&eacute;sus, &eacute;tant all&eacute; avec eux, n&#39;&eacute;tait gu&egrave;re &eacute;loign&eacute; de la maison, quand le centenier envoya des amis pour lui dire: Seigneur, ne prends pas tant de peine; car je ne suis pas digne que tu entres sous mon toit.</p>

<p><sup class="versenum">7&nbsp;</sup>C&#39;est aussi pour cela que je ne me suis pas cru digne d&#39;aller en personne vers toi. Mais dis un mot, et mon serviteur sera gu&eacute;ri.</p>

<p><sup class="versenum">8&nbsp;</sup>Car, moi qui suis soumis &agrave; des sup&eacute;rieurs, j&#39;ai des soldats sous mes ordres; et je dis &agrave; l&#39;un: Va! et il va; &agrave; l&#39;autre: Viens! et il vient; et &agrave; mon serviteur: Fais cela! et il le fait.</p>

<p><sup class="versenum">9&nbsp;</sup>Lorsque J&eacute;sus entendit ces paroles, il admira le centenier, et, se tournant vers la foule qui le suivait, il dit: Je vous le dis, m&ecirc;me en Isra&euml;l je n&#39;ai pas trouv&eacute; une aussi grande foi.</p>

<p><sup class="versenum">10&nbsp;</sup>De retour &agrave; la maison, les gens envoy&eacute;s par le centenier trouv&egrave;rent gu&eacute;ri le serviteur qui avait &eacute;t&eacute; malade.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/229.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 7:1-10&nbsp; </button>
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

<p>J&eacute;sus a fini d&#39;enseigner ses disciples. En revenant &agrave; Capernaum, Il rencontre un centenier romain, un officier militaire en charge de 100 hommes. Ce chef militaire romain a montr&eacute; un amour inhabituel et de la compassion pour son esclave malade en demandant l&#39;aide de J&eacute;sus. Son travail consistait &agrave; maintenir l&#39;ordre, &agrave; appliquer les lois et &agrave; s&#39;assurer que les imp&ocirc;ts &eacute;taient per&ccedil;us, mais Dieu l&#39;a utilis&eacute; pour instruire les leaders du mouvement. Ils ont appris:</p>

<ol>
	<li>qu&#39;un leader aime ceux qu&#39;ils dirigent.</li>
	<li>que le leader dirige avec humilit&eacute;, sachant qu&#39;il n&rsquo;est pas digne d&#39;honneur.</li>
	<li>un leader conduit par la foi, faisant confiance non pas &agrave; ce qu&#39;il peut voir mais au Dieu invisible.</li>
	<li>qu&#39;un leader ne doit jamais oublier qu&#39;il est sous autorit&eacute; et qu&#39;il rendra compte des personnes plac&eacute;es sous ses soins.</li>
</ol>

<p>Cet homme a &eacute;tonn&eacute; J&eacute;sus.</p>

<p>Pour une &eacute;tude approfondie <span class="popup-link" @click = "popUp('pop1')"> Matthieu 8:5-13</span>.</p>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">5&nbsp;</sup>Comme J&eacute;sus entrait dans Caperna&uuml;m, un centenier l&#39;aborda,</p>

<p><sup class="versenum">6&nbsp;</sup>le priant et disant: Seigneur, mon serviteur est couch&eacute; &agrave; la maison, atteint de paralysie et souffrant beaucoup.</p>

<p><sup class="versenum">7&nbsp;</sup>J&eacute;sus lui dit: J&#39;irai, et je le gu&eacute;rirai.</p>

<p><sup class="versenum">8&nbsp;</sup>Le centenier r&eacute;pondit: Seigneur, je ne suis pas digne que tu entres sous mon toit; mais dis seulement un mot, et mon serviteur sera gu&eacute;ri.</p>

<p><sup class="versenum">9&nbsp;</sup>Car, moi qui suis soumis &agrave; des sup&eacute;rieurs, j&#39;ai des soldats sous mes ordres; et je dis &agrave; l&#39;un: Va! et il va; &agrave; l&#39;autre: Viens! et il vient; et &agrave; mon serviteur: Fais cela! et il le fait.</p>

<p><sup class="versenum">10&nbsp;</sup>Apr&egrave;s l&#39;avoir entendu, J&eacute;sus fut dans l&#39;&eacute;tonnement, et il dit &agrave; ceux qui le suivaient: Je vous le dis en v&eacute;rit&eacute;, m&ecirc;me en Isra&euml;l je n&#39;ai pas trouv&eacute; une aussi grande foi.</p>

<p><sup class="versenum">11&nbsp;</sup>Or, je vous d&eacute;clare que plusieurs viendront de l&#39;orient et de l&#39;occident, et seront &agrave; table avec Abraham, Isaac et Jacob, dans le royaume des cieux.</p>

<p><sup class="versenum">12&nbsp;</sup>Mais les fils du royaume seront jet&eacute;s dans les t&eacute;n&egrave;bres du dehors, o&ugrave; il y aura des pleurs et des grincements de dents.</p>

<p><sup class="versenum">13&nbsp;</sup>Puis J&eacute;sus dit au centenier: Va, qu&#39;il te soit fait selon ta foi. Et &agrave; l&#39;heure m&ecirc;me le serviteur fut gu&eacute;ri.</p>
<!-- end bible --></div>

<p>&nbsp;</p>

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

			<td class="social" @click="share('lesson', 'Leadership et  and Autorité: ', '/content/M2/fra/multiply2/multiply229.html')">
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