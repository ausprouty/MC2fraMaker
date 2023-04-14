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
                        <div class="chapter_number ltr"><h1>7.</h1></div>
                        <div class="chapter_title ltr"><h1>Jésus et la Parole de Dieu</h1></div>
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
	<li>Lisez ou observez Luc 4:1-13 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 4:1-13</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>J&eacute;sus, rempli du Saint Esprit, revint du Jourdain, et il fut conduit par l&#39;Esprit dans le d&eacute;sert,</p>

<p><sup class="versenum">2&nbsp;</sup>o&ugrave; il fut tent&eacute; par le diable pendant quarante jours. Il ne mangea rien durant ces jours-l&agrave;, et, apr&egrave;s qu&#39;ils furent &eacute;coul&eacute;s, il eut faim.</p>

<p><sup class="versenum">3&nbsp;</sup>Le diable lui dit: Si tu es Fils de Dieu, ordonne &agrave; cette pierre qu&#39;elle devienne du pain.</p>

<p><sup class="versenum">4&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Il est &eacute;crit: L&#39;Homme ne vivra pas de pain seulement.</p>

<p><sup class="versenum">5&nbsp;</sup>Le diable, l&#39;ayant &eacute;lev&eacute;, lui montra en un instant tous les royaumes de la terre,</p>

<p><sup class="versenum">6&nbsp;</sup>et lui dit: Je te donnerai toute cette puissance, et la gloire de ces royaumes; car elle m&#39;a &eacute;t&eacute; donn&eacute;e, et je la donne &agrave; qui je veux.</p>

<p><sup class="versenum">7&nbsp;</sup>Si donc tu te prosternes devant moi, elle sera toute &agrave; toi.</p>

<p><sup class="versenum">8&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Il est &eacute;crit: Tu adoreras le Seigneur, ton Dieu, et tu le serviras lui seul.</p>

<p><sup class="versenum">9&nbsp;</sup>Le diable le conduisit encore &agrave; J&eacute;rusalem, le pla&ccedil;a sur le haut du temple, et lui dit: Si tu es Fils de Dieu, jette-toi d&#39;ici en bas; car il est &eacute;crit:</p>

<p><sup class="versenum">10&nbsp;</sup>Il donnera des ordres &agrave; ses anges &agrave; ton sujet, Afin qu&#39;ils te gardent;</p>

<p><sup class="versenum">11&nbsp;</sup>et: Ils te porteront sur les mains, De peur que ton pied ne heurte contre une pierre.</p>

<p><sup class="versenum">12&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Il es dit: Tu ne tenteras point le Seigneur, ton Dieu.</p>

<p><sup class="versenum">13&nbsp;</sup>Apr&egrave;s l&#39;avoir tent&eacute; de toutes ces mani&egrave;res, le diable s&#39;&eacute;loigna de lui jusqu&#39;&agrave; un moment favorable.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/207.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 4:1-13&nbsp; </button>
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

<p>J&eacute;sus &eacute;tait conduit dans le d&eacute;sert afin d&rsquo;&ecirc;tre tent&eacute; par Satan lui-m&ecirc;me. Apr&egrave;s 40 jours de tentation de toutes sortes, l&rsquo;ennemi vient &agrave; nouveau &agrave; J&eacute;sus. J&eacute;sus est maintenant faible, fatigu&eacute; et il a incroyablement faim. La tentation de Satan &eacute;tait une attaque directe de la v&eacute;rit&eacute; de la Parole de Dieu. C&rsquo;est la strat&eacute;gie de Satan depuis le commencement quand il l&rsquo;a utilis&eacute;e avec Adam et Eve (Gen&egrave;se 3). J&eacute;sus nous montre comment citer la promesse de Dieu pour contrer les attaques de l&rsquo;ennemi.</p>

<p>Pour une &eacute;tude approfondie : <span class="popup-link" @click = "popUp('pop1')"> Matthieu 4:1-11</span>.</p>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">1 </sup>Alors J&eacute;sus fut emmen&eacute; par l&#39;Esprit dans le d&eacute;sert, pour &ecirc;tre tent&eacute; par le diable.</p>

<p><sup class="versenum">2&nbsp;</sup>Apr&egrave;s avoir je&ucirc;n&eacute; quarante jours et quarante nuits, il eut faim.</p>

<p><sup class="versenum">3&nbsp;</sup>Le tentateur, s&#39;&eacute;tant approch&eacute;, lui dit: Si tu es Fils de Dieu, ordonne que ces pierres deviennent des pains.</p>

<p><sup class="versenum">4&nbsp;</sup>J&eacute;sus r&eacute;pondit: Il est &eacute;crit: L&#39;homme ne vivra pas de pain seulement, mais de toute parole qui sort de la bouche de Dieu.</p>

<p><sup class="versenum">5&nbsp;</sup>Le diable le transporta dans la ville sainte, le pla&ccedil;a sur le haut du temple,</p>

<p><sup class="versenum">6&nbsp;</sup>et lui dit: Si tu es Fils de Dieu, jette-toi en bas; car il est &eacute;crit: Il donnera des ordres &agrave; ses anges &agrave; ton sujet; Et ils te porteront sur les mains, De peur que ton pied ne heurte contre une pierre.</p>

<p><sup class="versenum">7&nbsp;</sup>J&eacute;sus lui dit: Il est aussi &eacute;crit: Tu ne tenteras point le Seigneur, ton Dieu.</p>

<p><sup class="versenum">8&nbsp;</sup>Le diable le transporta encore sur une montagne tr&egrave;s &eacute;lev&eacute;e, lui montra tous les royaumes du monde et leur gloire,</p>

<p><sup class="versenum">9&nbsp;</sup>et lui dit: Je te donnerai toutes ces choses, si tu te prosternes et m&#39;adores.</p>

<p><sup class="versenum">10&nbsp;</sup>J&eacute;sus lui dit: Retire-toi, Satan! Car il est &eacute;crit: Tu adoreras le Seigneur, ton Dieu, et tu le serviras lui seul.</p>

<p><sup class="versenum">11&nbsp;</sup>Alors le diable le laissa. Et voici, des anges vinrent aupr&egrave;s de J&eacute;sus, et le servaient.</p>
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

			<td class="social" @click="share('lesson', 'Jésus et la Parole de Dieu: ', '/content/M2/fra/multiply2/multiply207.html')">
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