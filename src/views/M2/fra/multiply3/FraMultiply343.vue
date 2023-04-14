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
                        <div class="chapter_number ltr"><h1>43.</h1></div>
                        <div class="chapter_title ltr"><h1>Visites aux disciples en allant à Jérusalem</h1></div>
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
	<li>Lisez ou observez Actes 21:1-26 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 21:1-26</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Nous nous embarqu&acirc;mes, apr&egrave;s nous &ecirc;tre s&eacute;par&eacute;s d&#39;eux, et nous all&acirc;mes directement &agrave; Cos, le lendemain &agrave; Rhodes, et de l&agrave; &agrave; Patara.</p>

<p><sup class="versenum">2&nbsp;</sup>Et ayant trouv&eacute; un navire qui faisait la travers&eacute;e vers la Ph&eacute;nicie, nous mont&acirc;mes et part&icirc;mes.</p>

<p><sup class="versenum">3&nbsp;</sup>Quand nous f&ucirc;mes en vue de l&#39;&icirc;le de Chypre, nous la laiss&acirc;mes &agrave; gauche, poursuivant notre route du c&ocirc;t&eacute; de la Syrie, et nous abord&acirc;mes &agrave; Tyr, o&ugrave; le b&acirc;timent devait d&eacute;charger sa cargaison.</p>

<p><sup class="versenum">4&nbsp;</sup>Nous trouv&acirc;mes les disciples, et nous rest&acirc;mes l&agrave; sept jours. Les disciples, pouss&eacute;s par l&#39;Esprit, disaient &agrave; Paul de ne pas monter &agrave; J&eacute;rusalem.</p>

<p><sup class="versenum">5&nbsp;</sup>Mais, lorsque nous f&ucirc;mes au terme des sept jours, nous nous achemin&acirc;mes pour partir, et tous nous accompagn&egrave;rent avec leur femme et leurs enfants jusque hors de la ville. Nous nous m&icirc;mes &agrave; genoux sur le rivage, et nous pri&acirc;mes.</p>

<p><sup class="versenum">6&nbsp;</sup>Puis, ayant pris cong&eacute; les uns des autres, nous mont&acirc;mes sur le navire, et ils retourn&egrave;rent chez eux.</p>

<p><sup class="versenum">7&nbsp;</sup>Achevant notre navigation, nous all&acirc;mes de Tyr &agrave; Ptol&eacute;ma&iuml;s, o&ugrave; nous salu&acirc;mes les fr&egrave;res, et pass&acirc;mes un jour avec eux.</p>

<p><sup class="versenum">8&nbsp;</sup>Nous part&icirc;mes le lendemain, et nous arriv&acirc;mes &agrave; C&eacute;sar&eacute;e. &Eacute;tant entr&eacute;s dans la maison de Philippe l&#39;&eacute;vang&eacute;liste, qui &eacute;tait l&#39;un des sept, nous loge&acirc;mes chez lui.</p>

<p><sup class="versenum">9&nbsp;</sup>Il avait quatre filles vierges qui proph&eacute;tisaient.</p>

<p><sup class="versenum">10&nbsp;</sup>Comme nous &eacute;tions l&agrave; depuis plusieurs jours, un proph&egrave;te, nomm&eacute; Agabus, descendit de Jud&eacute;e,</p>

<p><sup class="versenum">11&nbsp;</sup>et vint nous trouver. Il prit la ceinture de Paul, se lia les pieds et les mains, et dit: Voici ce que d&eacute;clare le Saint Esprit: L&#39;homme &agrave; qui appartient cette ceinture, les Juifs le lieront de la m&ecirc;me mani&egrave;re &agrave; J&eacute;rusalem, et le livreront entre les mains des pa&iuml;ens.</p>

<p><sup class="versenum">12&nbsp;</sup>Quand nous entend&icirc;mes cela, nous et ceux de l&#39;endroit, nous pri&acirc;mes Paul de ne pas monter &agrave; J&eacute;rusalem.</p>

<p><sup class="versenum">13&nbsp;</sup>Alors il r&eacute;pondit: Que faites-vous, en pleurant et en me brisant le coeur? Je suis pr&ecirc;t, non seulement &agrave; &ecirc;tre li&eacute;, mais encore &agrave; mourir &agrave; J&eacute;rusalem pour le nom du Seigneur J&eacute;sus.</p>

<p><sup class="versenum">14&nbsp;</sup>Comme il ne se laissait pas persuader, nous n&#39;insist&acirc;mes pas, et nous d&icirc;mes: Que la volont&eacute; du Seigneur se fasse!</p>

<p><sup class="versenum">15&nbsp;</sup>Apr&egrave;s ces jours-l&agrave;, nous f&icirc;mes nos pr&eacute;paratifs, et nous mont&acirc;mes &agrave; J&eacute;rusalem.</p>

<p><sup class="versenum">16&nbsp;</sup>Quelques disciples de C&eacute;sar&eacute;e vinrent aussi avec nous, et nous conduisirent chez un nomm&eacute; Mnason, de l&#39;&icirc;le de Chypre, ancien disciple, chez qui nous devions loger.</p>

<p><sup class="versenum">17&nbsp;</sup>Lorsque nous arriv&acirc;mes &agrave; J&eacute;rusalem, les fr&egrave;res nous re&ccedil;urent avec joie.</p>

<p><sup class="versenum">18&nbsp;</sup>Le lendemain, Paul se rendit avec nous chez Jacques, et tous les anciens s&#39;y r&eacute;unirent.</p>

<p><sup class="versenum">19&nbsp;</sup>Apr&egrave;s les avoir salu&eacute;s, il raconta en d&eacute;tail ce que Dieu avait fait au milieu des pa&iuml;ens par son minist&egrave;re.</p>

<p><sup class="versenum">20&nbsp;</sup>Quand ils l&#39;eurent entendu, ils glorifi&egrave;rent Dieu. Puis ils lui dirent: Tu vois, fr&egrave;re, combien de milliers de Juifs ont cru, et tous sont z&eacute;l&eacute;s pour la loi.</p>

<p><sup class="versenum">21&nbsp;</sup>Or, ils ont appris que tu enseignes &agrave; tous les Juifs qui sont parmi les pa&iuml;ens &agrave; renoncer &agrave; Mo&iuml;se, leur disant de ne pas circoncire les enfants et de ne pas se conformer aux coutumes.</p>

<p><sup class="versenum">22&nbsp;</sup>Que faire donc? Sans aucun doute la multitude se rassemblera, car on saura que tu es venu.</p>

<p><sup class="versenum">23&nbsp;</sup>C&#39;est pourquoi fais ce que nous allons te dire. Il y a parmi nous quatre hommes qui ont fait un voeu;</p>

<p><sup class="versenum">24&nbsp;</sup>prends-les avec toi, purifie-toi avec eux, et pourvois &agrave; leur d&eacute;pense, afin qu&#39;ils se rasent la t&ecirc;te. Et ainsi tous sauront que ce qu&#39;ils ont entendu dire sur ton compte est faux, mais que toi aussi tu te conduis en observateur de la loi.</p>

<p><sup class="versenum">25&nbsp;</sup>A l&#39;&eacute;gard des pa&iuml;ens qui ont cru, nous avons d&eacute;cid&eacute; et nous leur avons &eacute;crit qu&#39;ils eussent &agrave; s&#39;abstenir des viandes sacrifi&eacute;es aux idoles, du sang, des animaux &eacute;touff&eacute;s, et de l&#39;impudicit&eacute;.</p>

<p><sup class="versenum">26&nbsp;</sup>Alors Paul prit ces hommes, se purifia, et entra le lendemain dans le temple avec eux, pour annoncer &agrave; quel jour la purification serait accomplie et l&#39;offrande pr&eacute;sent&eacute;e pour chacun d&#39;eux.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/343.mp4" type="button" class="external-movie">
         Regardez Actes 21:1-26 </button>
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
	<li class="nobreak-final-final">Paul n&#39;&eacute;tait pas le seul &agrave; implanter des &eacute;glises. Nous apprenons de cette histoire qu&rsquo;il y a d&rsquo;autres communaut&eacute;s de croyants qui se sont form&eacute;es en dehors de l&rsquo;&oelig;uvre de Paul. &Agrave; C&eacute;sar&eacute;e, ils sont rest&eacute;s avec Philippe qui a t&eacute;moign&eacute; aupr&egrave;s des Samaritains et de l&#39;eunuque &eacute;thiopien (<span class="popup-link" @click = "popUp('pop3')"> Actes 8:40</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">40&nbsp;</sup>Philippe se trouva dans Azot, d&#39;o&ugrave; il alla jusqu&#39;&agrave; C&eacute;sar&eacute;e, en &eacute;vang&eacute;lisant toutes les villes par lesquelles il passait.</p>
	<!-- end bible --></div>
	Gr&acirc;ce aux filles de Philippe, nous apprenons que les femmes ont &eacute;galement re&ccedil;u des dons du Saint-Esprit comme la proph&eacute;tie. &Agrave; deux reprises, des proph&eacute;ties ont &eacute;t&eacute; donn&eacute;es par le Saint-Esprit sur le danger auquel Paul serait confront&eacute; &agrave; J&eacute;rusalem, mais ce n&#39;&eacute;tait pas nouveau pour Paul. Paul &eacute;tait contraint par l&#39;Esprit d&#39;aller &agrave; J&eacute;rusalem (<span class="popup-link" @click = "popUp('pop4')"> Actes 19:21</span>),&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">21&nbsp;</sup>Apr&egrave;s que ces choses se furent pass&eacute;es, Paul forma le projet d&#39;aller &agrave; J&eacute;rusalem, en traversant la Mac&eacute;doine et l&#39;Acha&iuml;e. Quand j&#39;aurai &eacute;t&eacute; l&agrave;, se disait-il, il faut aussi que je voie Rome.</p>
	<!-- end bible --></div>
	et il &eacute;tait averti que la pers&eacute;cution l&#39;attendait (<span class="popup-link" @click = "popUp('pop5')"> Actes 20: 22-23</span>).&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">22&nbsp;</sup>Et maintenant voici, li&eacute; par l&#39;Esprit, je vais &agrave; J&eacute;rusalem, ne sachant pas ce qui m&#39;y arrivera;</p>

	<p><sup class="versenum">23&nbsp;</sup>seulement, de ville en ville, l&#39;Esprit Saint m&#39;avertit que des liens et des tribulations m&#39;attendent.</p>
	<!-- end bible --></div>
	Paul avait accept&eacute; le fait que la souffrance faisait partie de la volont&eacute; du Seigneur pour lui. Les probl&egrave;mes d&rsquo;il y a huit ans plus t&ocirc;t concernant la pratique de la loi d&eacute;rangeaient toujours les croyants juifs de J&eacute;rusalem (<span class="popup-link" @click = "popUp('pop6')"> Actes 11</span>

	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><sup class="versenum">1 </sup>Les ap&ocirc;tres et les fr&egrave;res qui &eacute;taient dans la Jud&eacute;e apprirent que les pa&iuml;ens avaient aussi re&ccedil;u la parole de Dieu.</p>

	<p><sup class="versenum">2&nbsp;</sup>Et lorsque Pierre fut mont&eacute; &agrave; J&eacute;rusalem, les fid&egrave;les circoncis lui adress&egrave;rent des reproches,</p>

	<p><sup class="versenum">3&nbsp;</sup>en disant: Tu es entr&eacute; chez des incirconcis, et tu as mang&eacute; avec eux.</p>

	<p><sup class="versenum">4&nbsp;</sup>Pierre se mit &agrave; leur exposer d&#39;une mani&egrave;re suivie ce qui s&#39;&eacute;tait pass&eacute;.</p>

	<p><sup class="versenum">5&nbsp;</sup>Il dit: J&#39;&eacute;tais dans la ville de Jopp&eacute;, et, pendant que je priais, je tombai en extase et j&#39;eus une vision: un objet, semblable &agrave; une grande nappe attach&eacute;e par les quatre coins, descendait du ciel et vint jusqu&#39;&agrave; moi.</p>

	<p><sup class="versenum">6&nbsp;</sup>Les regards fix&eacute;s sur cette nappe, j&#39;examinai, et je vis les quadrup&egrave;des de la terre, les b&ecirc;tes sauvages, les reptiles, et les oiseaux du ciel.</p>

	<p><sup class="versenum">7&nbsp;</sup>Et j&#39;entendis une voix qui me disait: L&egrave;ve-toi, Pierre, tue et mange.</p>

	<p><sup class="versenum">8&nbsp;</sup>Mais je dis: Non, Seigneur, car jamais rien de souill&eacute; ni d&#39;impur n&#39;est entr&eacute; dans ma bouche.</p>

	<p><sup class="versenum">9&nbsp;</sup>Et pour la seconde fois la voix se fit entendre du ciel: Ce que Dieu a d&eacute;clar&eacute; pur, ne le regarde pas comme souill&eacute;.</p>

	<p><sup class="versenum">10&nbsp;</sup>Cela arriva jusqu&#39;&agrave; trois fois; puis tout fut retir&eacute; dans le ciel.</p>

	<p><sup class="versenum">11&nbsp;</sup>Et voici, aussit&ocirc;t trois hommes envoy&eacute;s de C&eacute;sar&eacute;e vers moi se pr&eacute;sent&egrave;rent devant la porte de la maison o&ugrave; j&#39;&eacute;tais.</p>

	<p><sup class="versenum">12&nbsp;</sup>L&#39;Esprit me dit de partir avec eux sans h&eacute;siter. Les six hommes que voici m&#39;accompagn&egrave;rent, et nous entr&acirc;mes dans la maison de Corneille.</p>

	<p><sup class="versenum">13&nbsp;</sup>Cet homme nous raconta comment il avait vu dans sa maison l&#39;ange se pr&eacute;sentant &agrave; lui et disant: Envoie &agrave; Jopp&eacute;, et fais venir Simon, surnomm&eacute; Pierre,</p>

	<p><sup class="versenum">14&nbsp;</sup>qui te dira des choses par lesquelles tu seras sauv&eacute;, toi et toute ta maison.</p>

	<p><sup class="versenum">15&nbsp;</sup>Lorsque je me fus mis &agrave; parler, le Saint Esprit descendit sur eux, comme sur nous au commencement.</p>

	<p><sup class="versenum">16&nbsp;</sup>Et je me souvins de cette parole du Seigneur: Jean a baptis&eacute; d&#39;eau, mais vous, vous serez baptis&eacute;s du Saint Esprit.</p>

	<p><sup class="versenum">17&nbsp;</sup>Or, puisque Dieu leur a accord&eacute; le m&ecirc;me don qu&#39;&agrave; nous qui avons cru au Seigneur J&eacute;sus Christ, pouvais-je, moi, m&#39;opposer &agrave; Dieu?</p>

	<p><sup class="versenum">18&nbsp;</sup>Apr&egrave;s avoir entendu cela, ils se calm&egrave;rent, et ils glorifi&egrave;rent Dieu, en disant: Dieu a donc accord&eacute; la repentance aussi aux pa&iuml;ens, afin qu&#39;ils aient la vie.</p>

	<p><sup class="versenum">19&nbsp;</sup>Ceux qui avaient &eacute;t&eacute; dispers&eacute;s par la pers&eacute;cution survenue &agrave; l&#39;occasion d&#39;&Eacute;tienne all&egrave;rent jusqu&#39;en Ph&eacute;nicie, dans l&#39;&icirc;le de Chypre, et &agrave; Antioche, annon&ccedil;ant la parole seulement aux Juifs.</p>

	<p><sup class="versenum">20&nbsp;</sup>Il y eut cependant parmi eux quelques hommes de Chypre et de Cyr&egrave;ne, qui, &eacute;tant venus &agrave; Antioche, s&#39;adress&egrave;rent aussi aux Grecs, et leur annonc&egrave;rent la bonne nouvelle du Seigneur J&eacute;sus.</p>

	<p><sup class="versenum">21&nbsp;</sup>La main du Seigneur &eacute;tait avec eux, et un grand nombre de personnes crurent et se convertirent au Seigneur.</p>

	<p><sup class="versenum">22&nbsp;</sup>Le bruit en parvint aux oreilles des membres de l&#39;&Eacute;glise de J&eacute;rusalem, et ils envoy&egrave;rent Barnabas jusqu&#39;&agrave; Antioche.</p>

	<p><sup class="versenum">23&nbsp;</sup>Lorsqu&#39;il fut arriv&eacute;, et qu&#39;il eut vu la gr&acirc;ce de Dieu, il s&#39;en r&eacute;jouit, et il les exhorta tous &agrave; rester d&#39;un coeur ferme attach&eacute;s au Seigneur.</p>

	<p><sup class="versenum">24&nbsp;</sup>Car c&#39;&eacute;tait un homme de bien, plein d&#39;Esprit Saint et de foi. Et une foule assez nombreuse se joignit au Seigneur.</p>

	<p><sup class="versenum">25&nbsp;</sup>Barnabas se rendit ensuite &agrave; Tarse, pour chercher Saul;</p>

	<p><sup class="versenum">26&nbsp;</sup>et, l&#39;ayant trouv&eacute;, il l&#39;amena &agrave; Antioche. Pendant toute une ann&eacute;e, ils se r&eacute;unirent aux assembl&eacute;es de l&#39;&Eacute;glise, et ils enseign&egrave;rent beaucoup de personnes. Ce fut &agrave; Antioche que, pour la premi&egrave;re fois, les disciples furent appel&eacute;s chr&eacute;tiens.</p>

	<p><sup class="versenum">27&nbsp;</sup>En ce temps-l&agrave;, des proph&egrave;tes descendirent de J&eacute;rusalem &agrave; Antioche.</p>

	<p><sup class="versenum">28&nbsp;</sup>L&#39;un deux, nomm&eacute; Agabus, se leva, et annon&ccedil;a par l&#39;Esprit qu&#39;il y aurait une grande famine sur toute la terre. Elle arriva, en effet, sous Claude.</p>

	<p><sup class="versenum">29&nbsp;</sup>Les disciples r&eacute;solurent d&#39;envoyer, chacun selon ses moyens, un secours aux fr&egrave;res qui habitaient la Jud&eacute;e.</p>

	<p><sup class="versenum">30&nbsp;</sup>Ils le firent parvenir aux anciens par les mains de Barnabas et de Saul.</p>
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<!-- end bible --></div>
	et <span class="popup-link" @click = "popUp('pop7')"> Actes 15</span>).&nbsp;

	<div class="popup invisible" id="pop7"><!-- begin bible -->
	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><sup class="versenum">1 </sup>Quelques hommes, venus de la Jud&eacute;e, enseignaient les fr&egrave;res, en disant: Si vous n&#39;&ecirc;tes circoncis selon le rite de Mo&iuml;se, vous ne pouvez &ecirc;tre sauv&eacute;s.</p>

	<p><sup class="versenum">2&nbsp;</sup>Paul et Barnabas eurent avec eux un d&eacute;bat et une vive discussion; et les fr&egrave;res d&eacute;cid&egrave;rent que Paul et Barnabas, et quelques-uns des leurs, monteraient &agrave; J&eacute;rusalem vers les ap&ocirc;tres et les anciens, pour traiter cette question.</p>

	<p><sup class="versenum">3&nbsp;</sup>Apr&egrave;s avoir &eacute;t&eacute; accompagn&eacute;s par l&#39;&Eacute;glise, ils poursuivirent leur route &agrave; travers la Ph&eacute;nicie et la Samarie, racontant la conversion des pa&iuml;ens, et ils caus&egrave;rent une grande joie &agrave; tous les fr&egrave;res.</p>

	<p><sup class="versenum">4&nbsp;</sup>Arriv&eacute;s &agrave; J&eacute;rusalem, ils furent re&ccedil;us par l&#39;&Eacute;glise, les ap&ocirc;tres et les anciens, et ils racont&egrave;rent tout ce que Dieu avait fait avec eux.</p>

	<p><sup class="versenum">5&nbsp;</sup>Alors quelques-uns du parti des pharisiens, qui avaient cru, se lev&egrave;rent, en disant qu&#39;il fallait circoncire les pa&iuml;ens et exiger l&#39;observation de la loi de Mo&iuml;se.</p>

	<p><sup class="versenum">6&nbsp;</sup>Les ap&ocirc;tres et les anciens se r&eacute;unirent pour examiner cette affaire.</p>

	<p><sup class="versenum">7&nbsp;</sup>Une grande discussion s&#39;&eacute;tant engag&eacute;e, Pierre se leva, et leur dit: Hommes fr&egrave;res, vous savez que d&egrave;s longtemps Dieu a fait un choix parmi vous, afin que, par ma bouche, les pa&iuml;ens entendissent la parole de l&#39;&Eacute;vangile et qu&#39;ils crussent.</p>

	<p><sup class="versenum">8&nbsp;</sup>Et Dieu, qui conna&icirc;t les coeurs, leur a rendu t&eacute;moignage, en leur donnant le Saint Esprit comme &agrave; nous;</p>

	<p><sup class="versenum">9&nbsp;</sup>il n&#39;a fait aucune diff&eacute;rence entre nous et eux, ayant purifi&eacute; leurs coeurs par la foi.</p>

	<p><sup class="versenum">10&nbsp;</sup>Maintenant donc, pourquoi tentez-vous Dieu, en mettant sur le cou des disciples un joug que ni nos p&egrave;res ni nous n&#39;avons pu porter?</p>

	<p><sup class="versenum">11&nbsp;</sup>Mais c&#39;est par la gr&acirc;ce du Seigneur J&eacute;sus que nous croyons &ecirc;tre sauv&eacute;s, de la m&ecirc;me mani&egrave;re qu&#39;eux.</p>

	<p><sup class="versenum">12&nbsp;</sup>Toute l&#39;assembl&eacute;e garda le silence, et l&#39;on &eacute;couta Barnabas et Paul, qui racont&egrave;rent tous les miracles et les prodiges que Dieu avait faits par eux au milieu des pa&iuml;ens.</p>

	<p><sup class="versenum">13&nbsp;</sup>Lorsqu&#39;ils eurent cess&eacute; de parler, Jacques prit la parole, et dit: Hommes fr&egrave;res, &eacute;coutez-moi!</p>

	<p><sup class="versenum">14&nbsp;</sup>Simon a racont&eacute; comment Dieu a d&#39;abord jet&eacute; les regards sur les nations pour choisir du milieu d&#39;elles un peuple qui port&acirc;t son nom.</p>

	<p><sup class="versenum">15&nbsp;</sup>Et avec cela s&#39;accordent les paroles des proph&egrave;tes, selon qu&#39;il est &eacute;crit:</p>

	<p><sup class="versenum">16&nbsp;</sup>Apr&egrave;s cela, je reviendrai, et je rel&egrave;verai de sa chute la tente de David, J&#39;en r&eacute;parerai les ruines, et je la redresserai,</p>

	<p><sup class="versenum">17&nbsp;</sup>Afin que le reste des hommes cherche le Seigneur, Ainsi que toutes les nations sur lesquelles mon nom est invoqu&eacute;, Dit le Seigneur, qui fait ces choses,</p>

	<p><sup class="versenum">18&nbsp;</sup>Et &agrave; qui elles sont connues de toute &eacute;ternit&eacute;.</p>

	<p><sup class="versenum">19&nbsp;</sup>C&#39;est pourquoi je suis d&#39;avis qu&#39;on ne cr&eacute;e pas des difficult&eacute;s &agrave; ceux des pa&iuml;ens qui se convertissent &agrave; Dieu,</p>

	<p><sup class="versenum">20&nbsp;</sup>mais qu&#39;on leur &eacute;crive de s&#39;abstenir des souillures des idoles, de l&#39;impudicit&eacute;, des animaux &eacute;touff&eacute;s et du sang.</p>

	<p><sup class="versenum">21&nbsp;</sup>Car, depuis bien des g&eacute;n&eacute;rations, Mo&iuml;se a dans chaque ville des gens qui le pr&ecirc;chent, puisqu&#39;on le lit tous les jours de sabbat dans les synagogues.</p>

	<p><sup class="versenum">22&nbsp;</sup>Alors il parut bon aux ap&ocirc;tres et aux anciens, et &agrave; toute l&#39;&Eacute;glise, de choisir parmi eux et d&#39;envoyer &agrave; Antioche, avec Paul et Barsabas, Jude appel&eacute; Barnabas et Silas, hommes consid&eacute;r&eacute;s entre les fr&egrave;res.</p>

	<p><sup class="versenum">23&nbsp;</sup>Ils les charg&egrave;rent d&#39;une lettre ainsi con&ccedil;ue: Les ap&ocirc;tres, les anciens, et les fr&egrave;res, aux fr&egrave;res d&#39;entre les pa&iuml;ens, qui sont &agrave; Antioche, en Syrie, et en Cilicie, salut!</p>

	<p><sup class="versenum">24&nbsp;</sup>Ayant appris que quelques hommes partis de chez nous, et auxquels nous n&#39;avions donn&eacute; aucun ordre, vous ont troubl&eacute;s par leurs discours et ont &eacute;branl&eacute; vos &acirc;mes,</p>

	<p><sup class="versenum">25&nbsp;</sup>nous avons jug&eacute; &agrave; propos, apr&egrave;s nous &ecirc;tre r&eacute;unis tous ensemble, de choisir des d&eacute;l&eacute;gu&eacute;s et de vous les envoyer avec nos bien-aim&eacute;s Barnabas et Paul,</p>

	<p><sup class="versenum">26&nbsp;</sup>ces hommes qui ont expos&eacute; leur vie pour le nom de notre Seigneur J&eacute;sus Christ.</p>

	<p><sup class="versenum">27&nbsp;</sup>Nous avons donc envoy&eacute; Jude et Silas, qui vous annonceront de leur bouche les m&ecirc;mes choses.</p>

	<p><sup class="versenum">28&nbsp;</sup>Car il a paru bon au Saint Esprit et &agrave; nous de ne vous imposer d&#39;autre charge que ce qui est n&eacute;cessaire,</p>

	<p><sup class="versenum">29&nbsp;</sup>savoir, de vous abstenir des viandes sacrifi&eacute;es aux idoles, du sang, des animaux &eacute;touff&eacute;s, et de l&#39;impudicit&eacute;, choses contre lesquelles vous vous trouverez bien de vous tenir en garde. Adieu.</p>

	<p><sup class="versenum">30&nbsp;</sup>Eux donc, ayant pris cong&eacute; de l&#39;&Eacute;glise, all&egrave;rent &agrave; Antioche, o&ugrave; ils remirent la lettre &agrave; la multitude assembl&eacute;e.</p>

	<p><sup class="versenum">31&nbsp;</sup>Apr&egrave;s l&#39;avoir lue, les fr&egrave;res furent r&eacute;jouis de l&#39;encouragement qu&#39;elle leur apportait.</p>

	<p><sup class="versenum">32&nbsp;</sup>Jude et Silas, qui &eacute;taient eux-m&ecirc;mes proph&egrave;tes, les exhort&egrave;rent et les fortifi&egrave;rent par plusieurs discours.</p>

	<p><sup class="versenum">33&nbsp;</sup>Au bout de quelque temps, les fr&egrave;res les laiss&egrave;rent en paix retourner vers ceux qui les avaient envoy&eacute;s.</p>

	<p><sup class="versenum">34&nbsp;</sup>Toutefois Silas trouva bon de rester.</p>

	<p><sup class="versenum">35&nbsp;</sup>Paul et Barnabas demeur&egrave;rent &agrave; Antioche, enseignant et annon&ccedil;ant, avec plusieurs autres, la bonne nouvelle de la parole du Seigneur.</p>

	<p><sup class="versenum">36&nbsp;</sup>Quelques jours s&#39;&eacute;coul&egrave;rent, apr&egrave;s lesquels Paul dit &agrave; Barnabas: Retournons visiter les fr&egrave;res dans toutes les villes o&ugrave; nous avons annonc&eacute; la parole du Seigneur, pour voir en quel &eacute;tat ils sont.</p>

	<p><sup class="versenum">37&nbsp;</sup>Barnabas voulait emmener aussi Jean, surnomm&eacute; Marc;</p>

	<p><sup class="versenum">38&nbsp;</sup>mais Paul jugea plus convenable de ne pas prendre avec eux celui qui les avait quitt&eacute;s depuis la Pamphylie, et qui ne les avait point accompagn&eacute;s dans leur oeuvre.</p>

	<p><sup class="versenum">39&nbsp;</sup>Ce dissentiment fut assez vif pour &ecirc;tre cause qu&#39;ils se s&eacute;par&egrave;rent l&#39;un de l&#39;autre. Et Barnabas, prenant Marc avec lui, s&#39;embarqua pour l&#39;&icirc;le de Chypre.</p>

	<p><sup class="versenum">40&nbsp;</sup>Paul fit choix de Silas, et partit, recommand&eacute; par les fr&egrave;res &agrave; la gr&acirc;ce du Seigneur.</p>

	<p><sup class="versenum">41&nbsp;</sup>Il parcourut la Syrie et la Cilicie, fortifiant les &Eacute;glises.</p>
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<!-- end bible --></div>
	Paul s&#39;est soumis aux demandes des dirigeants de J&eacute;rusalem de respecter la loi afin que les croyants locaux ne tr&eacute;buchent pas. Lisez <span class="popup-link" @click = "popUp('pop8')"> Romains 14:13-19</span>.&nbsp;

	<div class="popup invisible" id="pop8"><!-- begin bible -->
	<p><sup class="versenum">13&nbsp;</sup>Ne nous jugeons donc plus les uns les autres; mais pensez plut&ocirc;t &agrave; ne rien faire qui soit pour votre fr&egrave;re une pierre d&#39;achoppement ou une occasion de chute.</p>

	<p><sup class="versenum">14&nbsp;</sup>Je sais et je suis persuad&eacute; par le Seigneur J&eacute;sus que rien n&#39;est impur en soi, et qu&#39;une chose n&#39;est impure que pour celui qui la croit impure.</p>

	<p><sup class="versenum">15&nbsp;</sup>Mais si, pour un aliment, ton fr&egrave;re est attrist&eacute;, tu ne marches plus selon l&#39;amour: ne cause pas, par ton aliment, la perte de celui pour lequel Christ est mort.</p>

	<p><sup class="versenum">16&nbsp;</sup>Que votre privil&egrave;ge ne soit pas un sujet de calomnie.</p>

	<p><sup class="versenum">17&nbsp;</sup>Car le royaume de Dieu, ce n&#39;est pas le manger et le boire, mais la justice, la paix et la joie, par le Saint Esprit.</p>

	<p><sup class="versenum">18&nbsp;</sup>Celui qui sert Christ de cette mani&egrave;re est agr&eacute;able &agrave; Dieu et approuv&eacute; des hommes.</p>

	<p><sup class="versenum">19&nbsp;</sup>Ainsi donc, recherchons ce qui contribue &agrave; la paix et &agrave; l&#39;&eacute;dification mutuelle.</p>
	</div>
	</li>
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

			<td class="social" @click="share('lesson', 'Visites aux disciples en allant à Jérusalem: ', '/content/M2/fra/multiply3/multiply343.html')">
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