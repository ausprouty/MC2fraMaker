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
                        <div class="chapter_number ltr"><h1>31.</h1></div>
                        <div class="chapter_title ltr"><h1>Pardon et Leadership</h1></div>
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
	<li>Lisez ou observez Luc 7:36 - 8:3 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 7:36-8:3</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">36&nbsp;</sup>Un pharisien pria J&eacute;sus de manger avec lui. J&eacute;sus entra dans la maison du pharisien, et se mit &agrave; table.</p>

<p><sup class="versenum">37&nbsp;</sup>Et voici, une femme p&eacute;cheresse qui se trouvait dans la ville, ayant su qu&#39;il &eacute;tait &agrave; table dans la maison du pharisien, apporta un vase d&#39;alb&acirc;tre plein de parfum,</p>

<p><sup class="versenum">38&nbsp;</sup>et se tint derri&egrave;re, aux pieds de J&eacute;sus. Elle pleurait; et bient&ocirc;t elle lui mouilla les pieds de ses larmes, puis les essuya avec ses cheveux, les baisa, et les oignit de parfum.</p>

<p><sup class="versenum">39&nbsp;</sup>Le pharisien qui l&#39;avait invit&eacute;, voyant cela, dit en lui-m&ecirc;me: Si cet homme &eacute;tait proph&egrave;te, il conna&icirc;trait qui et de quelle esp&egrave;ce est la femme qui le touche, il conna&icirc;trait que c&#39;est une p&eacute;cheresse.</p>

<p><sup class="versenum">40&nbsp;</sup>J&eacute;sus prit la parole, et lui dit: Simon, j&#39;ai quelque chose &agrave; te dire. -Ma&icirc;tre, parle, r&eacute;pondit-il. -</p>

<p><sup class="versenum">41&nbsp;</sup>Un cr&eacute;ancier avait deux d&eacute;biteurs: l&#39;un devait cinq cents deniers, et l&#39;autre cinquante.</p>

<p><sup class="versenum">42&nbsp;</sup>Comme ils n&#39;avaient pas de quoi payer, il leur remit &agrave; tous deux leur dette. Lequel l&#39;aimera le plus?</p>

<p><sup class="versenum">43&nbsp;</sup>Simon r&eacute;pondit: Celui, je pense, auquel il a le plus remis. J&eacute;sus lui dit: Tu as bien jug&eacute;.</p>

<p><sup class="versenum">44&nbsp;</sup>Puis, se tournant vers la femme, il dit &agrave; Simon: Vois-tu cette femme? Je suis entr&eacute; dans ta maison, et tu ne m&#39;as point donn&eacute; d&#39;eau pour laver mes pieds; mais elle, elle les a mouill&eacute;s de ses larmes, et les a essuy&eacute;s avec ses cheveux.</p>

<p><sup class="versenum">45&nbsp;</sup>Tu ne m&#39;as point donn&eacute; de baiser; mais elle, depuis que je suis entr&eacute;, elle n&#39;a point cess&eacute; de me baiser les pieds.</p>

<p><sup class="versenum">46&nbsp;</sup>Tu n&#39;as point vers&eacute; d&#39;huile sur ma t&ecirc;te; mais elle, elle a vers&eacute; du parfum sur mes pieds.</p>

<p><sup class="versenum">47&nbsp;</sup>C&#39;est pourquoi, je te le dis, ses nombreux p&eacute;ch&eacute;s ont &eacute;t&eacute; pardonn&eacute;s: car elle a beaucoup aim&eacute;. Mais celui &agrave; qui on pardonne peu aime peu.</p>

<p><sup class="versenum">48&nbsp;</sup>Et il dit &agrave; la femme: Tes p&eacute;ch&eacute;s sont pardonn&eacute;s.</p>

<p><sup class="versenum">49&nbsp;</sup>Ceux qui &eacute;taient &agrave; table avec lui se mirent &agrave; dire en eux-m&ecirc;mes: Qui est celui-ci, qui pardonne m&ecirc;me les p&eacute;ch&eacute;s?</p>

<p><sup class="versenum">50&nbsp;</sup>Mais J&eacute;sus dit &agrave; la femme: Ta foi t&#39;a sauv&eacute;e, va en paix.</p>

<p><sup class="versenum">1 </sup>Ensuite, J&eacute;sus allait de ville en ville et de village en village, pr&ecirc;chant et annon&ccedil;ant la bonne nouvelle du royaume de Dieu.</p>

<p><sup class="versenum">2&nbsp;</sup>Les douze &eacute;taient avec de lui et quelques femmes qui avaient &eacute;t&eacute; gu&eacute;ries d&#39;esprits malins et de maladies: Marie, dite de Magdala, de laquelle &eacute;taient sortis sept d&eacute;mons,</p>

<p><sup class="versenum">3&nbsp;</sup>Jeanne, femme de Chuza, intendant d&#39;H&eacute;rode, Susanne, et plusieurs autres, qui l&#39;assistaient de leurs biens.</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/231.mp4" type="button" class="external-movie">
         Regardez Luc 7:36-8:3 </button>
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

<p>J&eacute;sus rencontre un pharisien curieux, Simon, qui vit &agrave; Caperna&uuml;m et qui suivait Son minist&egrave;re. Simon invite J&eacute;sus dans sa maison avec beaucoup d&#39;autres pharisiens. J&eacute;sus accepte l&#39;invitation pour un rendez-vous divin arrang&eacute; par le P&egrave;re pour atteindre ces hommes religieux et qui s&rsquo;auto-justifient. La soir&eacute;e commence et J&eacute;sus ne se voit pas offrir l&#39;hospitalit&eacute; normale que d&#39;autres auraient re&ccedil;ue en tant qu&#39;invit&eacute;s. Alors le P&egrave;re a envoy&eacute; une femme p&eacute;cheresse pour faire ces choses &agrave; l&rsquo;endroit de J&eacute;sus et Il en a profit&eacute; pour enseigner aux hommes le c&oelig;ur de ceux qui re&ccedil;oivent le pardon: ils sont honn&ecirc;tes avec leur besoin et ils sont humbles. Simon avait appris &agrave; couvrir ses p&eacute;ch&eacute;s. Nous devons faire attention &agrave; ne pas tomber dans ce m&ecirc;me pi&egrave;ge.</p>

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

			<td class="social" @click="share('lesson', 'Pardon et Leadership: ', '/content/M2/fra/multiply2/multiply231.html')">
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