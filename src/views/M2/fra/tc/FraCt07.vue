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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-tc-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>7.</h1></div>
                        <div class="chapter_title ltr"><h1>Comment aider à accomplir la Grande Commission</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <p>Aujourd&rsquo;hui nous l&rsquo;appellerions une rencontre strat&eacute;gique ; l&rsquo;Entra&icirc;neur et les &laquo; joueurs &raquo; ensemble formant un &laquo; regroupement &raquo; sur une montagne en Galil&eacute;e. Le Seigneur ressuscit&eacute; avait un plan, un plan tel qu&rsquo;il atteindra le monde entier. Les chr&eacute;tiens appellent cela la strat&eacute;gie globale &laquo; la Grande Commission &raquo; Ce qui avait &eacute;t&eacute; dit sur la montagne a affect&eacute; des g&eacute;n&eacute;rations sur des g&eacute;n&eacute;rations de croyants. Si cela n&rsquo;avait pas &eacute;t&eacute;, peu seraient aujourd&rsquo;hui ceux qui exp&eacute;rimentent l&rsquo;amour et le pardon de la gr&acirc;ce de Dieu.<br />
<br />
Les disciples se sont rapproch&eacute;s lorsque J&eacute;sus dit &laquo; Tout pouvoir m&rsquo;a &eacute;t&eacute; donn&eacute; dans le ciel et sur la terre. Allez, faites de toutes les nations des disciples, les baptisant au nom du P&egrave;re, du Fils et du Saint-Esprit, et enseignez-leur &agrave; observer tout ce que je vous ai prescrit. Et voici, je suis avec vous tous les jours, jusqu&rsquo;&agrave; la fin du monde. &raquo; (Matthieu 28:18-20). C&rsquo;est la plus grande promesse qui ait jamais &eacute;t&eacute; rapport&eacute;e.<br />
<br />
Dans ce chapitre, nous examinerons, le Qui, Quoi, Pourquoi, Quand, O&ugrave; et Comment de la Grande Commission.</p>

<h2>Qui a initi&eacute;la Grande Commission? Et&agrave;quis&rsquo;adressait-elle?</h2>

<p>Qui oserait affirmer &laquo; toute autorit&eacute;&hellip;dans le ciel et sur la terre &raquo;&nbsp; Il ne peut y avoir qu&rsquo;une seule r&eacute;ponse. Cela ne saurait &ecirc;tre que le Dieu unique/ (&eacute;tant) Lui-m&ecirc;me Homme, J&eacute;sus Christ, Le m&ecirc;me, Fils de Dieu. A la naissance de J&eacute;sus, Dieu devint homme. Il a permis que d&rsquo;autres hommes le mettent &agrave; mort sur une croix, mais trois jours plus tard, Il est ressuscit&eacute; des morts. Sa mort et Sa r&eacute;surrection ont sauv&eacute; la race humaine de la puissance du p&eacute;ch&eacute; et ont offert la vie &eacute;ternelle &agrave; tous ceux qui auront cru. Le r&eacute;sultat &eacute;tait une r&eacute;volution spirituelle qui a boulevers&eacute; le monde du premier si&egrave;cle et a chang&eacute; le cours de l&rsquo;histoire.<br />
<br />
Lorsque J&eacute;sus parcourait la terre, Il a eu le pouvoir de transformer des vies. Ce m&ecirc;me pouvoir qui transforme des vies est disponible aujourd&rsquo;hui. Sa vie s&rsquo;&eacute;tend sur des si&egrave;cles parce qu&rsquo;Il &eacute;tait&ndash;et est&ndash;Dieu! Bien que ce soit ces disciples qui l&rsquo;avaient entendu prononcer les paroles de la Grande Commission, leur impact continue de s&rsquo;appliquer &agrave; tous les Chr&eacute;tiens &agrave; travers l&rsquo;histoire.<br />
<br />
C&rsquo;est un plan surnaturel donn&eacute; par le Dieu infini &agrave; l&rsquo;homme fini. Tr&egrave;s souvent, nous-nous glissons dans l&rsquo;erreur de penser que les premiers Chr&eacute;tiens &eacute;taient diff&eacute;rents de nous &ndash;et qu&rsquo;ils avaient une qualit&eacute; de vie que nous ne pouvons pas atteindre. Mais les hommes et les femmes qui ont entendu les paroles de J&eacute;sus &eacute;taient des gens du commun, ordinaire, ouvriers, en proie aux m&ecirc;mes faiblesses que nous. Deux choses remarquables leur sont arriv&eacute;es.<br />
<br />
Premi&egrave;rement, ils ont connu un Seigneur ressuscit&eacute;, triomphant de la mort, celui-l&agrave; qui a v&eacute;cu au milieu d&rsquo;eux et a promis qu&rsquo;Il reviendra r&eacute;gner comme Roi sur toute la terre.<br />
<br />
Deuxi&egrave;mement, ils &eacute;taient remplis du Saint-Esprit.<br />
<br />
Nous avons les m&ecirc;mes opportunit&eacute;s d&rsquo;&ecirc;tre d&eacute;vou&eacute;s pour notre Seigneur ressuscit&eacute; qui revient. Son Esprit Saint est pr&ecirc;t &agrave; habiliter ceux d&rsquo;entre nous qui demandent &agrave; &ecirc;tre remplis de Lui. Nous avons la <em>m&ecirc;me capacit&eacute; de bouleverser le monde!</em> Nous pourrions enclencher une r&eacute;volution au 20&egrave;me Si&egrave;cle qui d&eacute;fiera tout ce que le monde a vu jusqu&rsquo;ici !</p>

<h2>Qu&rsquo;est-ce que la Grande Commission?</h2>

<p>Le commandement de notre Seigneur veut simplement dire gagner des c&oelig;urs pour J&eacute;sus, leur enseigner ce qu&rsquo;Il a enseign&eacute;, les &eacute;quiper pour les envoyer comme ambassadeurs, en masse , de mani&egrave;re que toutes les &acirc;mes que le monde contient entendraient le message annonc&eacute; par les anges la nuit o&ugrave; notre Seigneur &eacute;tait n&eacute; : &laquo; Je vous annonce une bonne nouvelle, qui sera pour tout le peuple le sujet d&rsquo;une grande joie: c&rsquo;est qu&rsquo;aujourd&rsquo;hui, dans la ville de David, il vous est n&eacute; un Sauveur, qui est le Christ, le Seigneur. &raquo; (LSG)<br />
<br />
Mais attendez un moment, vous dites que ce vieux monde contient presque 4 milliards de personnes. Vous n&rsquo;&ecirc;tes surement pas s&eacute;rieux au sujet du fait de parler de Christ &agrave; <em>tout le monde</em>. Oh Oui, nous le sommes !<br />
<br />
A ceux qui rient de la possibilit&eacute; d&rsquo;accomplir une t&acirc;che d&rsquo;une telle ampleur, nous citons les avantages qui entourent ceux d&rsquo;entre nous qui vivons dans ce si&egrave;cle passionnant. Consid&eacute;rez un moment le g&eacute;ant progr&egrave;s que la technologie a fait m&ecirc;me dans notre g&eacute;n&eacute;ration. Les m&eacute;dias ont ramen&eacute; les extr&eacute;mit&eacute;s de notre t&acirc;che &agrave; notre port&eacute;e. Laissez-moi vous donner un exemple.<br />
<br />
Un homme du nom de John Heyman a produit un film intitul&eacute; simplement <em>JESUS</em>. Depuis les ann&eacute;es de sa sortie, son impact &eacute;vang&eacute;lique de part le monde a &eacute;t&eacute; stup&eacute;fiant. Une copie de cette image peut &ecirc;tre parfaitement doubl&eacute;e en n&rsquo;importe quelle langue dans l&rsquo;intervalle d&rsquo;une semaine en utilisant des groupes &eacute;lectrog&egrave;nes, des studios d&rsquo;enregistrement Jungle et des acteurs de voix indig&egrave;nes.<br />
<br />
Le film doubl&eacute; a all&eacute;g&eacute; le besoin d&rsquo;un linguiste pour apprendre une langue tribale, de le r&eacute;duire &agrave; des symboles &eacute;crits, de traduire l&rsquo;Ecriture et d&rsquo;enseigner aux gens &agrave; lire afin que l&rsquo;&eacute;vangile puisse &ecirc;tre partag&eacute;&mdash; une t&acirc;che &eacute;norme dont la r&eacute;alisation prend des ann&eacute;es.<br />
<br />
<em>JESUS</em> a rendu possible &agrave; dix mille personnes de part la monde d&rsquo;avoir d&eacute;j&agrave; confi&eacute; leur vie &agrave; ce J&eacute;sus au sujet duquel ils ont appris. JESUS leur offre le message du salut dans leur propre langue. Vous sceptiques, nous sommes sur le bon chemin !</p>

<h2>Pourquoi les Chr&eacute;tiens Devraient-ils &Ecirc;tre Enti&egrave;rement D&eacute;vou&eacute;s &agrave; l&rsquo;Accomplissement de laGrande Commission ?</h2>

<p>Il y a au moins trois bonnes raisons :<br />
<br />
<em>1. Nous ob&eacute;issons parce que Christ nous a donn&eacute; le commandement d&rsquo;aller. </em>Le coach sportif pr&eacute;sente la liste de ses r&egrave;gles et ses normes &agrave; ses joueurs et dit : &laquo; Voici les choses que vous devez faire si vous esp&eacute;rez &ecirc;tre membres de l&rsquo;&eacute;quipe &raquo; Les joueurs respectent ces r&egrave;gles ou ils ne sont pas membres de l&rsquo;&eacute;quipe. Durant la guerre, le commandant en chef lance des ordres &agrave; ses soldats qui ob&eacute;issent sans discuter ou ils encourent le risque de la cour martiale, ou m&ecirc;me la mort. L&rsquo;autorit&eacute; de J&eacute;sus est bas&eacute; sur l&rsquo;amour, et soutenu par Dieu le P&egrave;re, et Il nous a laiss&eacute; un ordre &laquo; Allez !&raquo;. N&rsquo;osons pas prendre le commandement de notre Seigneur &agrave; la l&eacute;g&egrave;re.<br />
<br />
<em>2. Nous ob&eacute;issons parce que les hommes sont PERDUS sans Christ.</em> J&eacute;sus a dit &laquo;Je suis le chemin, la v&eacute;rit&eacute;, et la vie. Nul ne vient au P&egrave;re que par Moi. &raquo; (Jean 14:6). Cela peut avoir l&rsquo;air &eacute;troit, mais Dieu Lui.m&ecirc;me l&rsquo;a dit. Je n&rsquo;ose pas contester avec mon Seigneur.<br />
<br />
<em>3. Nous ob&eacute;issons parce que des c&oelig;urs ont faim de Dieu.</em> Depuis le commencement du minist&egrave;re de Campus pour Christ, nous avons &eacute;t&eacute; t&eacute;moins de la faim de l&rsquo;homme pour Dieu, d&eacute;montr&eacute;e de mille et une fa&ccedil;ons. Comme faisant partie de notre programme de formation &agrave; travers le monde, les &eacute;tudiants passent des heures chaque semaine &agrave; &eacute;vang&eacute;liser en t&ecirc;te &agrave; t&ecirc;te au sein des communaut&eacute;s locales, sur les plages et dans des rassemblements publics. Ce n&rsquo;est pas rare qu&rsquo;au cours d&rsquo;un seul apr&egrave;s-midi des centaines de personnes prient pour recevoir Christ.<br />
<br />
Plus de trois milles Afro-Am&eacute;ricains au centre-sud de Los Angeles ont re&ccedil;u Christ par contact personnel &agrave; travers quelques 1600 &eacute;quipiers et des &eacute;tudiants ouvriers. Plus de 2000 ont invit&eacute; Christ dans leurs vies en un jour de t&eacute;moignage sur les plages de la Californie du Sud.<br />
<br />
Dans des conditions semblables, 9000 stagiaires Kor&eacute;ens ont parl&eacute; de Christ &agrave; 42000 personnes au cours d&rsquo;un seul apr&egrave;s-midi de t&eacute;moignage. Seize milles personnes ont exprim&eacute; le d&eacute;sir de recevoir Christ, et 4000 se sont appropri&eacute;s la puissance du Saint-Esprit par la foi.</p>

<h2>Quand Est-Ce Que la Grande Commission sera Accomplie ?</h2>

<p>Seul J&eacute;sus et Son P&egrave;re le savent quand et comment cela sera accompli. Toutefois, puisqu&rsquo;Il nous a donn&eacute; le commandement, supposez qu&rsquo;Il veut que nous poursuivions l&rsquo;accomplissement de Son dessein au sein de chaque g&eacute;n&eacute;ration. &mdash; un processus continu pour l&rsquo;accomplissement de la Grande Commission.<br />
<br />
S&rsquo;il est absolument n&eacute;cessaire qu&rsquo;elle soit accomplie, c&rsquo;est maintenant qu&rsquo;il faut agir. Nous devons commencer maintenant et nous y employer chaque jour &ndash;comme un style de vie &mdash;pour transmettre l&rsquo;amour de Dieu et Son pardon &agrave; ceux que nos vies touchent. Comme l&rsquo;ap&ocirc;tre Paul l&rsquo;a &eacute;crit en Colossiens 1 :28 &laquo; C&rsquo;est lui que nous annon&ccedil;ons, exhortant tout homme, et instruisant tout homme en toute sagesse. Depuis le moment o&ugrave; nous nous r&eacute;veillons le matin jusqu&rsquo;au moment o&ugrave; nous-nous couchons la nuit, notre premi&egrave;re priorit&eacute; est de partager la nouvelle la plus joyeuse qui ait jamais &eacute;t&eacute; annonc&eacute;e &agrave; des c&oelig;urs qui ont soif de l&rsquo;entendre.</p>

<h2>O&ugrave; Est-Ce-Que Nous Accomplissons la Grande Commission ?</h2>

<p>Nous devons atteindre le monde entier&mdash; une impossibilit&eacute; d&eacute;courageante pour de simples &ecirc;tres humains. Mais J&eacute;sus nous a &eacute;tabli une strat&eacute;gie &agrave; suivre. Peu avant qu&rsquo;Il ne monte au ciel, J&eacute;sus a dit &agrave; Ses disciples, &laquo; vous serez mes t&eacute;moins &agrave; J&eacute;rusalem, dans toute la Jud&eacute;e, dans la Samarie, et jusqu&rsquo;aux extr&eacute;mit&eacute;s de la terre. &raquo; (LSG)<br />
<br />
J&eacute;rusalem abritait les disciples, la Jud&eacute;e, ville voisine, qui &eacute;tait aussi un territoire familier. Mais la Samarie &eacute;tait la terre des Pa&iuml;ens, des &eacute;trangers qui ne savaient rien aux croyances Juifs, c&rsquo;&eacute;tait le lieu o&ugrave; commence &laquo; l&rsquo;extr&eacute;mit&eacute; de la terre&raquo;<br />
<br />
O&ugrave; est-ce que &laquo; J&eacute;rusalem &raquo; commence pour nous ? Cet endroit o&ugrave; commencent tous les voyages: &agrave; la maison. Nos vies dans nos maisons peuvent refl&eacute;ter l&rsquo;amour que J&eacute;sus transmet par notre canal. Partant de l&agrave;, cet amour se r&eacute;pandra dans notre voisinage, nos campus et salles de classe, nos lieux de travail et dans tout ce en quoi nous nous engageons. La prochaine &eacute;tape logique sera vers &laquo; Jud&eacute;e &raquo; nos communaut&eacute;s et &eacute;tats (divisions territoriales), nos nations. Et de l&agrave;, ce sera un petit pas de plus pour entrer en &laquo; Samarie et l&rsquo;extr&eacute;mit&eacute; du monde &raquo; La Grande Commission reste immobile &agrave; moins que nous ne reconnaissions notre part et ne devenions personnellement impliqu&eacute;s dans nos maisons et communaut&eacute;s et finalement dans notre monde !<br />
<br />
Oh, quel moment passionnant pour que les Chr&eacute;tiens s&rsquo;impliquent. Nous sommes &agrave; deux doigts du plus grand r&eacute;veil spirituel depuis la Pentec&ocirc;te ! Ce que les hommes voient comme une heure sombre et sans promesse est en effet une heure de destin&eacute;e pour les Chr&eacute;tiens, une heure pour laquelle nous sommes n&eacute;s! Il est temps de briller comme les lumi&egrave;res d&rsquo;un phare et mettre en marche une r&eacute;volution spirituelle de grande ampleur et qui r&eacute;v&egrave;lera &agrave; l&rsquo;humanit&eacute; le glorieux &eacute;vangile de Christ, la r&eacute;ponse &agrave; toutes les questions.<br />
<br />
Ne restez pas derri&egrave;re! Soyez impliqu&eacute;s! Jouez votre partition pour aider &agrave; accomplir la Grande Commission dans cette g&eacute;n&eacute;ration !</p>

<h2>Comment Partageons-Nous Ce Que nous Avons?</h2>

<p>Partout les hommes sont perdus, et nous qui appartenons au Christ avons la r&eacute;ponse. Lorsqu&rsquo;Il a dit &laquo; Allez &raquo;, J&eacute;sus a rendu clair que cette &laquo; r&eacute;ponse &raquo; doit &ecirc;tre transmise. C&rsquo;est Sa volont&eacute; que nous soyons activement impliqu&eacute;s pour aider &agrave; accomplir Son commandement. &ndash;Sa Grande Commission. Et jusque l&agrave;, la question subsiste. Qu&rsquo;est-ce que Dieu veut que je fasse ? Comment vais-je commencer ?<br />
<br />
Nous commen&ccedil;ons en d&eacute;veloppant des strat&eacute;gies individuelles, personnelles qui s&rsquo;int&egrave;grent directement avec la strat&eacute;gie globale de notre Seigneur. C&rsquo;est de cette seule fa&ccedil;on que cette grande t&acirc;che sera accomplie.<br />
<br />
Et qu&rsquo;est-ce qu&rsquo;une strat&eacute;gie personnelle ? C&rsquo;est un plan d&rsquo;action individuel pour accomplir un objectif sp&eacute;cifique. Puisque notre objectif est d&rsquo;aider &agrave; accomplir le commandement de Christ, l&rsquo;&eacute;vang&eacute;lisation et le discipolat doit faire partie de nos plans personnels&ndash; ajouter au Corps de J&eacute;sus-Christ., et multiplier les croyants.<br />
<br />
L&rsquo;addition spirituelle est simple : Un croyant +l&rsquo;&eacute;vangile + un non croyant = deux croyants. La multiplication spirituelle est un peu diff&eacute;rente: La formule est : Un croyant +un nouveau croyant +discip&ocirc;lat = deux croyants qui &eacute;vang&eacute;lisent et qui font d&rsquo;autres des disciples. La multiplication spirituelle consiste &agrave; faire d&eacute;lib&eacute;r&eacute;ment des disciples les nouveaux croyants afin qu&rsquo;ils puissent continuer &agrave; &eacute;vang&eacute;liser et faire d&rsquo;autres des disciples.<br />
<br />
Paul a particuli&egrave;rement recommand&eacute; ce principe &agrave; Timoth&eacute;e, son &laquo; fils &raquo; dans la foi, quand il a dit &laquo; Et ce que tu as entendu de moi en pr&eacute;sence de beaucoup de t&eacute;moins, <em>confie-le &agrave; des hommes fid&egrave;les, qui soient capables de l&rsquo;enseigner aussi &agrave; d&rsquo;autres.</em> &raquo;(2 Timoth&eacute;e 2:2).</p>

<h2>Ayezune Strat&eacute;gie Personnelle</h2>

<p>Une strat&eacute;gie personnelle nous permet d&rsquo;avancer dans l&rsquo;ob&eacute;issance pour aider &agrave; accomplir la Grande Commission. Paul a dit : &laquo; Il n&rsquo;est pas de soldat qui s&rsquo;embarrasse des affaires de la vie, s&rsquo;il veut plaire &agrave; celui qui l&rsquo;a enr&ocirc;l&eacute; &raquo; (2Timoth&eacute;e 2:4).<br />
<br />
&laquo; D&rsquo;accord &raquo; vous d&icirc;tes, &laquo; Je suis convaincu que j&rsquo;ai besoin d&rsquo;avoir une strat&eacute;gie personnelle. Mais o&ugrave; vais-je commencer &agrave; d&eacute;velopper un plan personnel qui sera effectif dans ma vie ? Permettez-moi de faire quelques suggestions simples bas&eacute;es sur l&rsquo;Ecriture.<br />
<br />
<em>Soyez engag&eacute;s envers Christ et remplis du Saint Esprit. </em>Parmi les millions de personnes qui sont actives dans les &eacute;glises, un pourcentage effrayant est soit incertain qu&rsquo;ils sont n&eacute;s de nouveau, ou vivent une vie charnelle frustr&eacute;e, si &eacute;loign&eacute;s qu&rsquo;ils ne peuvent pas &ecirc;tre utilis&eacute;s par Dieu jusqu&rsquo;&agrave; ce qu&rsquo;ils ne Lui confient leurs vies. Si vous &ecirc;tes en proie &agrave; un manque de foi, occupez.vous en. Apprenez comment faire confiance &agrave; Dieu et partant de l&agrave; Il prendra le relais.<br />
<br />
Prier en ayant foi que Dieu vous guidera dans le d&eacute;veloppement de votre strat&eacute;gie personnelle. Demandez-Lui de vous r&eacute;v&eacute;ler un plan efficace pour atteindre votre cadre d&rsquo;influence imm&eacute;diate avec l&rsquo;&eacute;vangile. Il y a d&eacute;j&agrave; un plan con&ccedil;u, votre r&ocirc;le c&rsquo;est la d&eacute;couverte, et elle se produit g&eacute;n&eacute;ralement peu &agrave; peu.<br />
<br />
La vie de J&eacute;sus &eacute;tait un exemple parfait de la d&eacute;couverte du plan du P&egrave;re. Il pr&eacute;sentait chaque d&eacute;cision importante &agrave; Dieu et attendait la direction divine &agrave; chaque tournant d&eacute;cisif. En priant, attendez.vous &agrave; ce que Dieu pourvoit la strat&eacute;gie, la sagesse et la force pour la mettre en &oelig;uvre. Une foi qui esp&egrave;re plait &agrave; Dieu.<br />
<br />
Esquisser le plan que Dieu a r&eacute;v&eacute;l&eacute; en r&eacute;ponse &agrave; vos pri&egrave;res. Faites la liste des personnes et groupes sp&eacute;cifiques que vous connaissez dans votre vie et d&eacute;veloppez un plan en vue de les atteindre chacun. Commencez par votre famille. Votre maison plus que tout autre endroit refl&egrave;tera votre t&eacute;moignage.<br />
<br />
Faites confiance &agrave; Dieu pour qu&rsquo;Il vous remplisse de Son Esprit afin que vos actions t&eacute;moignent de ce qu&rsquo;Il a fait en vous.<br />
<br />
Faites le plan d&rsquo;atteindre les gens de votre lieu de travail. Cherchez ceux que vous savez qu&rsquo;ils sont Chr&eacute;tiens, et demandez-leur de se joindre &agrave; vous pour &eacute;vang&eacute;liser votre service ou votre usine. Dans votre &eacute;glise, rendez vous disponibles pour enseigner l&rsquo;&eacute;cole de Dimanche et pour faire partie (ou commencez) des &eacute;quipes d&rsquo;&eacute;vang&eacute;lisation porte &agrave; porte. Soyez un encouragement pour d&rsquo;autres membres de votre &eacute;glise.<br />
<br />
Invitez les voisins chez vous pour prendre un caf&eacute; ou une collation avec une tendance &eacute;vang&eacute;lique. Dites aux autres ce que Christ a fait dans votre vie, et qu&rsquo;Il peut faire le m&ecirc;me dans les leurs.<br />
<br />
Apprenez tout ce dont vous &ecirc;tes capables pour aider &agrave; accomplir une strat&eacute;gie personnelle. Des milliers d&rsquo;&eacute;tudiants, de la&iuml;cs et de pasteurs profitent de la formation et des mat&eacute;riels rendus disponibles &agrave; travers Campus pour Christ chaque ann&eacute;e. Ils apprennent des aptitudes efficaces pour gagner des hommes et des femmes &agrave; Christ et pour les &eacute;difier dans la foi et les envoyer &agrave; l&rsquo;&oelig;uvre avec la bonne nouvelle de l&rsquo;amour et du pardon de Dieu. Des choses telles que les Instituts de Formation au Leadership pour les &eacute;tudiants de l&rsquo;Universit&eacute; et &eacute;l&egrave;ves du Lyc&eacute;e, les Instituts d&rsquo;Evang&eacute;lisation pour La&iuml;cs et Pasteurs peuvent dispenser des cours tant fondamentaux qu&rsquo;avanc&eacute;s tout au long de l&rsquo;ann&eacute;e.<br />
<br />
N&rsquo;attendez pas. Ecrivez votre strat&eacute;gie personnelle aujourd&rsquo;hui. Faites la liste du nom des personnes que Dieu a plac&eacute;es dans votre esprit et dans votre c&oelig;ur. Partagez Christ avec eux et ajoutez au corps des croyants. Faites des demandes &agrave; Dieu pour les noms sp&eacute;cifiques de ceux qu&rsquo;Il aimerait que vous formiez pour multiplier spirituellement avec vous.<br />
<br />
Pratiquer l&rsquo;&eacute;vang&eacute;lisation agressive. Prenez l&rsquo;initiative de remplir votre part de la Grande Commission &agrave; l&rsquo;endroit m&ecirc;me o&ugrave; vous habitez. R&eacute;clamez les membres de votre famille, vos amis, vos voisins et vos associ&eacute;s professionnels pour Christ dans la pri&egrave;re. Puis pr&eacute;sentez-leur l&rsquo;Evangile. Parlez-leur de l&rsquo;amour et du pardon que J&eacute;sus attend de leur donner et accordez-leur une opportunit&eacute; de Le recevoir.<br />
<br />
Partagez votre foi comme un style de vie. Cela deviendra naturel de parler de Christ avec tous ceux que vous rencontrez. A mesure que les personnes qui sont sur votre liste commencent &agrave; Lui faire confiance en tant que Seigneur et Sauveur, faites d&rsquo;eux des disciples et impliquez-les dans le processus de la multiplication spirituelle. Encouragez-les &agrave; se joindre &agrave; vous dans l&rsquo;effort de saturer votre zone enti&egrave;re avec le message de J&eacute;sus-Christ.<br />
<br />
En mettant en application votre strat&eacute;gie personnelle localement, demandez la direction de Dieu pour &eacute;tendre votre pens&eacute;e au-del&agrave; des objectifs locaux &agrave; des responsabilit&eacute;s mondiales. D&eacute;couvrez des moyens par lesquels vous pouvez devenir un Chr&eacute;tien dont la conscience est ouverte sur le monde et apporter une contribution pour aider &agrave; r&eacute;pandre l&rsquo;&eacute;vangile &agrave; l&rsquo;&eacute;tranger. Enqu&eacute;rez-vous du programme des missions dans votre &eacute;glise.<br />
<br />
En ces jours de changement et de chaos, que les Chr&eacute;tiens n&rsquo;osent pas &ecirc;tre satisfaits du statuquo ou des affaires comme d&rsquo;habitude. Qui et o&ugrave; que vous soyez, quand vous vous mettez &agrave; la disposition de Dieu, attendez-vous &agrave; &ecirc;tre utilis&eacute;s pour changer le monde. Des c&oelig;urs transform&eacute;s font un monde transform&eacute;. J&eacute;sus est sp&eacute;cialis&eacute; dans la transformation des vies, mais Il ne peut atteindre les hommes et les femmes qu&rsquo;&agrave; travers nous. Laissez-le commencer par vous !<br />
<br />
Si votre d&eacute;sir est d&rsquo;aider &agrave; accomplir la Grande Commission, faites v&ocirc;tre la pri&egrave;re suivante :<br />
<br />
<em>Cher P&egrave;re, Je suis disponible pour que Tu te serves de moi comme tu le souhaite. &OElig;uvre &agrave; travers moi pour apporter le message de Ton amour et de Ton pardon aux c&oelig;urs qui ont soif de l&rsquo;entendre. Purifie-moi, habilite.moi, utilise-moi pour apporter honneur et gloire &agrave; Ton nom. Rends-moi capable par ton Esprit Saint de donner le meilleur de moi-m&ecirc;me pour aider &agrave; accomplir Ta Grande Commission en mon temps. Dans le beau nom de J&eacute;sus, j&rsquo;ai demand&eacute; ceci. Amen. </em><br />
<br />
Si vous avez fait cette pri&egrave;re, je vous souhaite que Dieu vous accompagne dans vos efforts. Pr&eacute;parez-vous pour une grande aventure. En investissant votre temps, votre talent et votre tr&eacute;sor, vous accomplirez ainsi la Grande Commission de Christ dans cette g&eacute;n&eacute;ration. Votre engagement est envers Christ pas envers Campus pour Christ, mais si en quelque mani&egrave;re nous pouvons aider, nous sommes dispos&eacute;s &agrave; vous servir. Par le pouvoir de Christ habitant en nous, vous pouvez contribuer &agrave; changer le monde !</p>

<h2>Application</h2>

<ol>
	<li>Qu&rsquo;avez-vous aim&eacute; le plus (qu&rsquo;est-ce qui a retenu votre attention)?</li>
	<li>Pourquoi?</li>
	<li>A qui devrais-je transmettre cette information ?</li>
</ol>

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


<p>Adapt&eacute; de Les Messages Transmissibles par Bill Bright. &copy; Cru. Tous droits r&eacute;serv&eacute;s</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Comment aider à accomplir la Grande Commission: ', '/content/M2/fra/tc/ct07.html')">
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