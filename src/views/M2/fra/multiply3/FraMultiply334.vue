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
                        <div class="chapter_number ltr"><h1>34.</h1></div>
                        <div class="chapter_title ltr"><h1>Implantation d'église dans la capitale de la Macédoine (Thessalonique)</h1></div>
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
	<li>Lisez ou observez Actes 17:1-15 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 17:1-15</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Paul et Silas pass&egrave;rent par Amphipolis et Apollonie, et ils arriv&egrave;rent &agrave; Thessalonique, o&ugrave; les Juifs avaient une synagogue.</p>

<p><sup class="versenum">2&nbsp;</sup>Paul y entra, selon sa coutume. Pendant trois sabbats, il discuta avec eux, d&#39;apr&egrave;s les &Eacute;critures,</p>

<p><sup class="versenum">3&nbsp;</sup>expliquant et &eacute;tablissant que le Christ devait souffrir et ressusciter des morts. Et J&eacute;sus que je vous annonce, disait-il, c&#39;est lui qui est le Christ.</p>

<p><sup class="versenum">4&nbsp;</sup>Quelques-uns d&#39;entre eux furent persuad&eacute;s, et se joignirent &agrave; Paul et &agrave; Silas, ainsi qu&#39;une grande multitude de Grecs craignant Dieu, et beaucoup de femmes de qualit&eacute;.</p>

<p><sup class="versenum">5&nbsp;</sup>Mais les Juifs, jaloux prirent avec eux quelques m&eacute;chants hommes de la populace, provoqu&egrave;rent des attroupements, et r&eacute;pandirent l&#39;agitation dans la ville. Ils se port&egrave;rent &agrave; la maison de Jason, et ils cherch&egrave;rent Paul et Silas, pour les amener vers le peuple.</p>

<p><sup class="versenum">6&nbsp;</sup>Ne les ayant pas trouv&eacute;s, ils tra&icirc;n&egrave;rent Jason et quelques fr&egrave;res devant les magistrats de la ville, en criant: Ces gens, qui ont boulevers&eacute; le monde, sont aussi venus ici, et Jason les a re&ccedil;us.</p>

<p><sup class="versenum">7&nbsp;</sup>Ils agissent tous contre les &eacute;dits de C&eacute;sar, disant qu&#39;il y a un autre roi, J&eacute;sus.</p>

<p><sup class="versenum">8&nbsp;</sup>Par ces paroles ils &eacute;murent la foule et les magistrats,</p>

<p><sup class="versenum">9&nbsp;</sup>qui ne laiss&egrave;rent aller Jason et les autres qu&#39;apr&egrave;s avoir obtenu d&#39;eux une caution.</p>

<p><sup class="versenum">10&nbsp;</sup>Aussit&ocirc;t les fr&egrave;res firent partir de nuit Paul et Silas pour B&eacute;r&eacute;e. Lorsqu&#39;ils furent arriv&eacute;s, ils entr&egrave;rent dans la synagogue des Juifs.</p>

<p><sup class="versenum">11&nbsp;</sup>Ces Juifs avaient des sentiments plus nobles que ceux de Thessalonique; ils re&ccedil;urent la parole avec beaucoup d&#39;empressement, et ils examinaient chaque jour les &Eacute;critures, pour voir si ce qu&#39;on leur disait &eacute;tait exact.</p>

<p><sup class="versenum">12&nbsp;</sup>Plusieurs d&#39;entre eux crurent, ainsi que beaucoup de femmes grecques de distinction, et beaucoup d&#39;hommes.</p>

<p><sup class="versenum">13&nbsp;</sup>Mais, quand les Juifs de Thessalonique surent que Paul annon&ccedil;ait aussi &agrave; B&eacute;r&eacute;e la parole de Dieu, ils vinrent y agiter la foule.</p>

<p><sup class="versenum">14&nbsp;</sup>Alors les fr&egrave;res firent aussit&ocirc;t partir Paul du c&ocirc;t&eacute; de la mer; Silas et Timoth&eacute;e rest&egrave;rent &agrave; B&eacute;r&eacute;e.</p>

<p><sup class="versenum">15&nbsp;</sup>Ceux qui accompagnaient Paul le conduisirent jusqu&#39;&agrave; Ath&egrave;nes. Puis ils s&#39;en retourn&egrave;rent, charg&eacute;s de transmettre &agrave; Silas et &agrave; Timoth&eacute;e l&#39;ordre de le rejoindre au plus t&ocirc;t.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/334.mp4" type="button" class="external-movie">
         Regardez Actes 17:1-15 </button>
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
	<li class="nobreak-final-final">Paul et son &eacute;quipe ont quitt&eacute; Philippes et se sont rendus dans la capitale provinciale de Thessalonique. Paul a continu&eacute; sa coutume qui est d&#39;aller &agrave; la synagogue pour trouver des personnes spirituellement int&eacute;ress&eacute;es. Une &eacute;glise a &eacute;t&eacute; implant&eacute;e avec des juifs, de nombreux hommes grecs et des femmes de qualit&eacute; de la ville. Le mod&egrave;le de pers&eacute;cution a souvent commenc&eacute; avec la jalousie des leaders juifs locaux. Cette fois, ils ont port&eacute; plainte contre l&rsquo;&eacute;quipe d&rsquo;avoir provoqu&eacute; des troubles sociaux. Les autorit&eacute;s locales ont obtenu une caution de Jason, qui accueillait Paul et son &eacute;quipe (<span class="popup-link" @click = "popUp('pop3')"> Actes 17: 7-9</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">7&nbsp;</sup>Ils agissent tous contre les &eacute;dits de C&eacute;sar, disant qu&#39;il y a un autre roi, J&eacute;sus.</p>

	<p><sup class="versenum">8&nbsp;</sup>Par ces paroles ils &eacute;murent la foule et les magistrats,</p>

	<p><sup class="versenum">9&nbsp;</sup>qui ne laiss&egrave;rent aller Jason et les autres qu&#39;apr&egrave;s avoir obtenu d&#39;eux une caution.</p>
	<!-- end bible --></div>
	Paul et son &eacute;quipe ont &eacute;t&eacute; contraints de quitter la jeune &eacute;glise apr&egrave;s seulement quelques mois. Cependant, leur mission d&#39;implantation d&#39;&eacute;glises s&#39;est poursuivie &agrave; B&eacute;r&eacute;e, une autre ville de la province de Mac&eacute;doine. Les B&eacute;r&eacute;ens ont appris avec empressement de Paul et examinaient les &Eacute;critures pour confirmer la v&eacute;racit&eacute; de ce que Paul enseignait. La nouvelle &eacute;glise &eacute;tait compos&eacute;e de nombreux Juifs b&eacute;r&eacute;ens, de femmes grecques de distinction et beaucoup d&rsquo;hommes grecs. Les Juifs hostiles de Thessalonique ont poursuivi l&#39;&eacute;quipe de la mission jusqu&#39;&agrave; B&eacute;r&eacute;e, for&ccedil;ant finalement Paul &agrave; quitter la province.</li>
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

			<td class="social" @click="share('lesson', 'Implantation d\'église dans la capitale de la Macédoine (Thessalonique): ', '/content/M2/fra/multiply3/multiply334.html')">
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