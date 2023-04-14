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
                        <div class="chapter_number ltr"><h1>51.</h1></div>
                        <div class="chapter_title ltr"><h1>Faire confiance à Jésus dans les circonstances dangereuses</h1></div>
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
	<li>Lisez ou observez Actes 27:1-26 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 27:1-26</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Lorsqu&#39;il fut d&eacute;cid&eacute; que nous nous embarquerions pour l&#39;Italie, on remit Paul et quelques autres prisonniers &agrave; un centenier de la cohorte Auguste, nomm&eacute; Julius.</p>

<p><sup class="versenum">2&nbsp;</sup>Nous mont&acirc;mes sur un navire d&#39;Adramytte, qui devait c&ocirc;toyer l&#39;Asie, et nous part&icirc;mes, ayant avec nous Aristarque, Mac&eacute;donien de Thessalonique.</p>

<p><sup class="versenum">3&nbsp;</sup>Le jour suivant, nous abord&acirc;mes &agrave; Sidon; et Julius, qui traitait Paul avec bienveillance, lui permit d&#39;aller chez ses amis et de recevoir leurs soins.</p>

<p><sup class="versenum">4&nbsp;</sup>Partis de l&agrave;, nous longe&acirc;mes l&#39;&icirc;le de Chypre, parce que les vents &eacute;taient contraires.</p>

<p><sup class="versenum">5&nbsp;</sup>Apr&egrave;s avoir travers&eacute; la mer qui baigne la Cilicie et la Pamphylie, nous arriv&acirc;mes &agrave; Myra en Lycie.</p>

<p><sup class="versenum">6&nbsp;</sup>Et l&agrave;, le centenier, ayant trouv&eacute; un navire d&#39;Alexandrie qui allait en Italie, nous y fit monter.</p>

<p><sup class="versenum">7&nbsp;</sup>Pendant plusieurs jours nous navigu&acirc;mes lentement, et ce ne fut pas sans difficult&eacute; que nous atteign&icirc;mes la hauteur de Cnide, o&ugrave; le vent ne nous permit pas d&#39;aborder. Nous pass&acirc;mes au-dessous de l&#39;&icirc;le de Cr&egrave;te, du c&ocirc;t&eacute; de Salmone.</p>

<p><sup class="versenum">8&nbsp;</sup>Nous la c&ocirc;toy&acirc;mes avec peine, et nous arriv&acirc;mes &agrave; un lieu nomm&eacute; Beaux Ports, pr&egrave;s duquel &eacute;tait la ville de Las&eacute;e.</p>

<p><sup class="versenum">9&nbsp;</sup>Un temps assez long s&#39;&eacute;tait &eacute;coul&eacute;, et la navigation devenait dangereuse, car l&#39;&eacute;poque m&ecirc;me du je&ucirc;ne &eacute;tait d&eacute;j&agrave; pass&eacute;e.</p>

<p><sup class="versenum">10&nbsp;</sup>C&#39;est pourquoi Paul avertit les autres, en disant: O hommes, je vois que la navigation ne se fera pas sans p&eacute;ril et sans beaucoup de dommage, non seulement pour la cargaison et pour le navire, mais encore pour nos personnes.</p>

<p><sup class="versenum">11&nbsp;</sup>Le centenier &eacute;couta le pilote et le patron du navire plut&ocirc;t que les paroles de Paul.</p>

<p><sup class="versenum">12&nbsp;</sup>Et comme le port n&#39;&eacute;tait pas bon pour hiverner, la plupart furent d&#39;avis de le quitter pour t&acirc;cher d&#39;atteindre Ph&eacute;nix, port de Cr&egrave;te qui regarde le sud-ouest et le nord-ouest, afin d&#39;y passer l&#39;hiver.</p>

<p><sup class="versenum">13&nbsp;</sup>Un l&eacute;ger vent du sud vint &agrave; souffler, et, se croyant ma&icirc;tres de leur dessein, ils lev&egrave;rent l&#39;ancre et c&ocirc;toy&egrave;rent de pr&egrave;s l&#39;&icirc;le de Cr&egrave;te.</p>

<p><sup class="versenum">14&nbsp;</sup>Mais bient&ocirc;t un vent imp&eacute;tueux, qu&#39;on appelle Euraquilon, se d&eacute;cha&icirc;na sur l&#39;&icirc;le.</p>

<p><sup class="versenum">15&nbsp;</sup>Le navire fut entra&icirc;n&eacute;, sans pouvoir lutter contre le vent, et nous nous laiss&acirc;mes aller &agrave; la d&eacute;rive.</p>

<p><sup class="versenum">16&nbsp;</sup>Nous pass&acirc;mes au-dessous d&#39;une petite &icirc;le nomm&eacute;e Clauda, et nous e&ucirc;mes de la peine &agrave; nous rendre ma&icirc;tres de la chaloupe;</p>

<p><sup class="versenum">17&nbsp;</sup>apr&egrave;s l&#39;avoir hiss&eacute;e, on se servit des moyens de secours pour ceindre le navire, et, dans la crainte de tomber sur la Syrte, on abaissa les voiles. C&#39;est ainsi qu&#39;on se laissa emporter par le vent.</p>

<p><sup class="versenum">18&nbsp;</sup>Comme nous &eacute;tions violemment battus par la temp&ecirc;te, le lendemain on jeta la cargaison &agrave; la mer,</p>

<p><sup class="versenum">19&nbsp;</sup>et le troisi&egrave;me jour nous y lan&ccedil;&acirc;mes de nos propres mains les agr&egrave;s du navire.</p>

<p><sup class="versenum">20&nbsp;</sup>Le soleil et les &eacute;toiles ne parurent pas pendant plusieurs jours, et la temp&ecirc;te &eacute;tait si forte que nous perd&icirc;mes enfin toute esp&eacute;rance de nous sauver.</p>

<p><sup class="versenum">21&nbsp;</sup>On n&#39;avait pas mang&eacute; depuis longtemps. Alors Paul, se tenant au milieu d&#39;eux, leur dit: O hommes, il fallait m&#39;&eacute;couter et ne pas partir de Cr&egrave;te, afin d&#39;&eacute;viter ce p&eacute;ril et ce dommage.</p>

<p><sup class="versenum">22&nbsp;</sup>Maintenant je vous exhorte &agrave; prendre courage; car aucun de vous ne p&eacute;rira, et il n&#39;y aura de perte que celle du navire.</p>

<p><sup class="versenum">23&nbsp;</sup>Un ange du Dieu &agrave; qui j&#39;appartiens et que je sers m&#39;est apparu cette nuit,</p>

<p><sup class="versenum">24&nbsp;</sup>et m&#39;a dit: Paul, ne crains point; il faut que tu comparaisses devant C&eacute;sar, et voici, Dieu t&#39;a donn&eacute; tous ceux qui naviguent avec toi.</p>

<p><sup class="versenum">25&nbsp;</sup>C&#39;est pourquoi, &ocirc; hommes, rassurez-vous, car j&#39;ai cette confiance en Dieu qu&#39;il en sera comme il m&#39;a &eacute;t&eacute; dit.</p>

<p><sup class="versenum">26&nbsp;</sup>Mais nous devons &eacute;chouer sur une &icirc;le.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/351.mp4" type="button" class="external-movie">
         Regardez Actes 27:1-26 </button>
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
	<li class="nobreak-final-final">Luc et Aristarque, l&#39;un des dirigeants Thessaloniciens, venu &agrave; J&eacute;rusalem avec Paul il y a deux ans, se sont joints aux prisonniers transf&eacute;r&eacute;s vers Rome (v2). Les marins ont pris un grand risque en essayant de naviguer trop tard pendant la saison des voyages, mettant tout le monde dans des situations tr&egrave;s dangereuses. Autant que nous sachions, Paul, Luc et Aristarque &eacute;taient les seuls chr&eacute;tiens &agrave; bord avec environ 273 non-chr&eacute;tiens (<span class="popup-link" @click = "popUp('pop3')"> Actes 27:37</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">37&nbsp;</sup>Nous &eacute;tions, dans le navire, deux cent soixante-seize personnes en tout.</p>
	<!-- end bible --></div>
	Nous voyons le c&oelig;ur de compassion que J&eacute;sus a pour les gens lorsqu&#39;il a promis de sauver Paul et tous ceux qui sont sur le navire. Paul a mis en &oelig;uvre sa confiance en J&eacute;sus devant tout le monde, mais il &eacute;tait aussi tr&egrave;s pratique dans la fa&ccedil;on dont il r&eacute;pondait aux besoins des gens. La confiance et la pi&eacute;t&eacute; n&#39;excluaient pas le bon sens au sujet de ce dont les gens avaient besoin. Bien qu&rsquo;&eacute;tant dans une posture humiliante d&#39;un prisonnier, le caract&egrave;re de leadership et la comp&eacute;tence de Paul sont clairement mis en &eacute;vidence ici. Les autres ont commenc&eacute; &agrave; l&#39;&eacute;couter. Nous apprenons que notre influence ne d&eacute;pend pas de notre position dans la vie.</li>
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

			<td class="social" @click="share('lesson', 'Faire confiance à Jésus dans les circonstances dangereuses: ', '/content/M2/fra/multiply3/multiply351.html')">
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