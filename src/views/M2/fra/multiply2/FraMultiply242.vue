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
                        <div class="chapter_number ltr"><h1>42.</h1></div>
                        <div class="chapter_title ltr"><h1>Jésus, Lumière du Monde</h1></div>
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
	<li>Lisez ou observez Jean 9:1-41 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 9</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>J&eacute;sus vit, en passant, un homme aveugle de naissance.</p>

<p><sup class="versenum">2&nbsp;</sup>Ses disciples lui firent cette question: Rabbi, qui a p&eacute;ch&eacute;, cet homme ou ses parents, pour qu&#39;il soit n&eacute; aveugle?</p>

<p><sup class="versenum">3&nbsp;</sup>J&eacute;sus r&eacute;pondit: Ce n&#39;est pas que lui ou ses parents aient p&eacute;ch&eacute;; mais c&#39;est afin que les oeuvres de Dieu soient manifest&eacute;es en lui.</p>

<p><sup class="versenum">4&nbsp;</sup>Il faut que je fasse, tandis qu&#39;il est jour, les oeuvres de celui qui m&#39;a envoy&eacute;; la nuit vient, o&ugrave; personne ne peut travailler.</p>

<p><sup class="versenum">5&nbsp;</sup>Pendant que je suis dans le monde, je suis la lumi&egrave;re du monde.</p>

<p><sup class="versenum">6&nbsp;</sup>Apr&egrave;s avoir dit cela, il cracha &agrave; terre, et fit de la boue avec sa salive. Puis il appliqua cette boue sur les yeux de l&#39;aveugle,</p>

<p><sup class="versenum">7&nbsp;</sup>et lui dit: Va, et lave-toi au r&eacute;servoir de Silo&eacute; (nom qui signifie envoy&eacute;). Il y alla, se lava, et s&#39;en retourna voyant clair.</p>

<p><sup class="versenum">8&nbsp;</sup>Ses voisins et ceux qui auparavant l&#39;avaient connu comme un mendiant disaient: N&#39;est-ce pas l&agrave; celui qui se tenait assis et qui mendiait?</p>

<p><sup class="versenum">9&nbsp;</sup>Les uns disaient: C&#39;est lui. D&#39;autres disaient: Non, mais il lui ressemble. Et lui-m&ecirc;me disait: C&#39;est moi.</p>

<p><sup class="versenum">10&nbsp;</sup>Ils lui dirent donc: Comment tes yeux ont-ils &eacute;t&eacute; ouverts?</p>

<p><sup class="versenum">11&nbsp;</sup>Il r&eacute;pondit: L&#39;Homme qu&#39;on appelle J&eacute;sus a fait de la boue, a oint mes yeux, et m&#39;a dit: Va au r&eacute;servoir de Silo&eacute;, et lave-toi. J&#39;y suis all&eacute;, je me suis lav&eacute;, et j&#39;ai recouvr&eacute; la vue.</p>

<p><sup class="versenum">12&nbsp;</sup>Ils lui dirent: O&ugrave; est cet homme? Il r&eacute;pondit: Je ne sais.</p>

<p><sup class="versenum">13&nbsp;</sup>Ils men&egrave;rent vers les pharisiens celui qui avait &eacute;t&eacute; aveugle.</p>

<p><sup class="versenum">14&nbsp;</sup>Or, c&#39;&eacute;tait un jour de sabbat que J&eacute;sus avait fait de la boue, et lui avait ouvert les yeux.</p>

<p><sup class="versenum">15&nbsp;</sup>De nouveau, les pharisiens aussi lui demand&egrave;rent comment il avait recouvr&eacute; la vue. Et il leur dit: Il a appliqu&eacute; de la boue sur mes yeux, je me suis lav&eacute;, et je vois.</p>

<p><sup class="versenum">16&nbsp;</sup>Sur quoi quelques-uns des pharisiens dirent: Cet homme ne vient pas de Dieu, car il n&#39;observe pas le sabbat. D&#39;autres dirent: Comment un homme p&eacute;cheur peut-il faire de tels miracles?</p>

<p><sup class="versenum">17&nbsp;</sup>Et il y eut division parmi eux. Ils dirent encore &agrave; l&#39;aveugle: Toi, que dis-tu de lui, sur ce qu&#39;il t&#39;a ouvert les yeux? Il r&eacute;pondit: C&#39;est un proph&egrave;te.</p>

<p><sup class="versenum">18&nbsp;</sup>Les Juifs ne crurent point qu&#39;il e&ucirc;t &eacute;t&eacute; aveugle et qu&#39;il e&ucirc;t recouvr&eacute; la vue jusqu&#39;&agrave; ce qu&#39;ils eussent fait venir ses parents.</p>

<p><sup class="versenum">19&nbsp;</sup>Et ils les interrog&egrave;rent, disant: Est-ce l&agrave; votre fils, que vous dites &ecirc;tre n&eacute; aveugle? Comment donc voit-il maintenant?</p>

<p><sup class="versenum">20&nbsp;</sup>Ses parents r&eacute;pondirent: Nous savons que c&#39;est notre fils, et qu&#39;il est n&eacute; aveugle;</p>

<p><sup class="versenum">21&nbsp;</sup>mais comment il voit maintenant, ou qui lui a ouvert les yeux, c&#39;est ce que nous ne savons. Interrogez-le lui-m&ecirc;me, il a de l&#39;&acirc;ge, il parlera de ce qui le concerne.</p>

<p><sup class="versenum">22&nbsp;</sup>Ses parents dirent cela parce qu&#39;ils craignaient les Juifs; car les Juifs &eacute;taient d&eacute;j&agrave; convenus que, si quelqu&#39;un reconnaissait J&eacute;sus pour le Christ, il serait exclu de la synagogue.</p>

<p><sup class="versenum">23&nbsp;</sup>C&#39;est pourquoi ses parents dirent: Il a de l&#39;&acirc;ge, interrogez-le lui-m&ecirc;me.</p>

<p><sup class="versenum">24&nbsp;</sup>Les pharisiens appel&egrave;rent une seconde fois l&#39;homme qui avait &eacute;t&eacute; aveugle, et ils lui dirent: Donne gloire &agrave; Dieu; nous savons que cet homme est un p&eacute;cheur.</p>

<p><sup class="versenum">25&nbsp;</sup>Il r&eacute;pondit: S&#39;il est un p&eacute;cheur, je ne sais; je sais une chose, c&#39;est que j&#39;&eacute;tais aveugle et que maintenant je vois.</p>

<p><sup class="versenum">26&nbsp;</sup>Ils lui dirent: Que t&#39;a-t-il fait? Comment t&#39;a-t-il ouvert les yeux?</p>

<p><sup class="versenum">27&nbsp;</sup>Il leur r&eacute;pondit: Je vous l&#39;ai d&eacute;j&agrave; dit, et vous n&#39;avez pas &eacute;cout&eacute;; pourquoi voulez-vous l&#39;entendre encore? Voulez-vous aussi devenir ses disciples?</p>

<p><sup class="versenum">28&nbsp;</sup>Ils l&#39;injuri&egrave;rent et dirent: C&#39;est toi qui es son disciple; nous, nous sommes disciples de Mo&iuml;se.</p>

<p><sup class="versenum">29&nbsp;</sup>Nous savons que Dieu a parl&eacute; &agrave; Mo&iuml;se; mais celui-ci, nous ne savons d&#39;o&ugrave; il est.</p>

<p><sup class="versenum">30&nbsp;</sup>Cet homme leur r&eacute;pondit: Il est &eacute;tonnant que vous ne sachiez d&#39;o&ugrave; il est; et cependant il m&#39;a ouvert les yeux.</p>

<p><sup class="versenum">31&nbsp;</sup>Nous savons que Dieu n&#39;exauce point les p&eacute;cheurs; mais, si quelqu&#39;un l&#39;honore et fait sa volont&eacute;, c&#39;est celui l&agrave; qu&#39;il l&#39;exauce.</p>

<p><sup class="versenum">32&nbsp;</sup>Jamais on n&#39;a entendu dire que quelqu&#39;un ait ouvert les yeux d&#39;un aveugle-n&eacute;.</p>

<p><sup class="versenum">33&nbsp;</sup>Si cet homme ne venait pas de Dieu, il ne pourrait rien faire.</p>

<p><sup class="versenum">34&nbsp;</sup>Ils lui r&eacute;pondirent: Tu es n&eacute; tout entier dans le p&eacute;ch&eacute;, et tu nous enseignes! Et ils le chass&egrave;rent.</p>

<p><sup class="versenum">35&nbsp;</sup>J&eacute;sus apprit qu&#39;ils l&#39;avaient chass&eacute;; et, l&#39;ayant rencontr&eacute;, il lui dit: Crois-tu au Fils de Dieu?</p>

<p><sup class="versenum">36&nbsp;</sup>Il r&eacute;pondit: Et qui est-il, Seigneur, afin que je croie en lui?</p>

<p><sup class="versenum">37&nbsp;</sup>Tu l&#39;as vu, lui dit J&eacute;sus, et celui qui te parle, c&#39;est lui.</p>

<p><sup class="versenum">38&nbsp;</sup>Et il dit: Je crois, Seigneur. Et il se prosterna devant lui.</p>

<p><sup class="versenum">39&nbsp;</sup>Puis J&eacute;sus dit: Je suis venu dans ce monde pour un jugement, pour que ceux qui ne voient point voient, et que ceux qui voient deviennent aveugles.</p>

<p><sup class="versenum">40&nbsp;</sup>Quelques pharisiens qui &eacute;taient avec lui, ayant entendu ces paroles, lui dirent: Nous aussi, sommes-nous aveugles?</p>

<p><sup class="versenum">41&nbsp;</sup>J&eacute;sus leur r&eacute;pondit: Si vous &eacute;tiez aveugles, vous n&#39;auriez pas de p&eacute;ch&eacute;. Mais maintenant vous dites: Nous voyons. C&#39;est pour cela que votre p&eacute;ch&eacute; subsiste.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/242.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 9:1-41&nbsp; </button>
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

<p>J&eacute;sus assiste &agrave; une autre f&ecirc;te, la f&ecirc;te de la d&eacute;dicace ou des lumi&egrave;res. C&#39;&eacute;tait pour se rappeler un moment o&ugrave; Dieu a fait un miracle pour fournir la lumi&egrave;re dans les lampes quand il n&#39;y avait pas assez d&#39;huile pour qu&#39;elles continuent &agrave; br&ucirc;ler. Lors de la f&ecirc;te, J&eacute;sus rencontre un homme aveugle de naissance. La plupart des gens croyaient que si quelqu&#39;un souffrait c&#39;&eacute;tait parce qu&#39;il ou un de ses proches avait p&eacute;ch&eacute;. J&eacute;sus va choquer ceux qui l&#39;entourent en disant que cet homme est n&eacute; aveugle afin que la gloire de Dieu soit manifest&eacute;e dans sa vie. Il a enseign&eacute; un principe &eacute;tonnant, Dieu peut permettre la souffrance afin qu&#39;il puisse &ecirc;tre glorifi&eacute;. Il est important de se rappeler que Dieu est le centre de la vie. Il tire la gloire en r&eacute;pondant aux gens quand ils l&#39;appellent dans le besoin. Une le&ccedil;on pour nous est de faire attention &agrave; ne juger personne parce qu&rsquo;elle souffre, ce n&#39;est peut- &ecirc;tre pas &agrave; cause de tout ce qu&#39;il a fait, mais &agrave; cause de l&rsquo;&oelig;uvre que Dieu accomplira dans sa vie.</p>

</div>

<p class="year">[Hiver 29 AP. J.-C]</p>

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

			<td class="social" @click="share('lesson', 'Jésus, Lumière du Monde: ', '/content/M2/fra/multiply2/multiply242.html')">
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