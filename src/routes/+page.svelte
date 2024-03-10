<script context="module" lang="ts">
  import Header from "$lib/header.svelte";
  import UserProfile from "$lib/userProfile.svelte";
  import UserArticleComponent from "$lib/userArticleComponent.svelte";
  import UserExperienceComponent from "$lib/userExperienceComponent.svelte";

  //assuming this data is coming from the backend and the fields are mandatory 
  export interface UserData {
    userName: string;
    about: string;
    currentCompany: string;
    currentPosition: string;
    currentCompanyIcon: string;
    websiteLink: string;
    profileImage: string;
    pastExperience: Array<UserExperience|ArticleArray>;
  }
  export interface UserExperience {
    companyName: string;
    position: string;
    joiningDate: string;
    companyIcon: string;
    location: string;
    Time:string;
    remote: boolean;
  }
  export interface ArticleArray{
    articles: Array<UserArticle>;
    date: string;
  }
  export interface UserArticle {
    articleMonth: string;
    articleContent: string;
    articleImage: string;
  }

  let userData: UserData = {
    userName: "Krishna Kiran",
    about: "Co-Founder and CEO at Duggup - Social network for people in tech. Ex-Amazon Head of Engineering. I write hot-takes on building a business, shipping delightful products and accelerating product and career growth.",
    currentCompany: "Duggup",
    currentPosition: "Co-Founder and CEO",
    currentCompanyIcon: "/logoIcon.svg",
    websiteLink: "https://www.krishnakiran.com/",
    profileImage: "/userImage.svg",
    pastExperience: [
      {
        articles:[
          {
            articleMonth: "Dec 2023",
            articleContent: "No amount of technology can convert a bad story into a good story.",
            articleImage: "https://s3-alpha-sig.figma.com/img/ccdc/bd9b/5b2f7dca180260dd9a121e21e4ccb158?Expires=1710720000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=dOWBi6OHLSab0NnAaNUUXQkXB5~7u0al1jfpXxNgA0tlnAiMVIOqESi-PMhBkg8XTcM3Avu-~kmWy9R46SPhcRdaDFIUnCnnTw-Oi~LymMYl4APflb5NEEJnEIch5ZUw2mtvpnsXPg0AJtbR3wGRzECIOzQVAluoDWOxQDzqiDZPZBgbXQ0iWXyR9ecwlUY4LHEkdZ-ZeDkU3bU39Pw87Vt2Q7QsE9wY2baFiD7KLkYWCuoNm2DF6KoN5KkW6eKcM8C102~UPvSom0~4dxklFMeV6S4ZI3glmKDZVMJXXAcYsGQRYv-z8QtklRtpuE7ZuNM4CeF85M4OW5L8Ob848A__"
          },
          {
            articleMonth: "Dec 2023",
            articleContent: "Most people don't have original ideas. Here is how Sam Altman pushes himself to have unpopular ideas.",
            articleImage: "https://s3-alpha-sig.figma.com/img/25ac/166c/37888417ccf24a1991743ef364aea246?Expires=1710720000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=RA144wBULxFqs3giTkSpv~K-Ks6LwHcjUK5-FvbiNwtV-jHgMdfBBDDeiqT0I-MqARSKmHtjVNYI0SsWQ6X~K586jbuM0UpnxJUxtYZRph6lw6DyuPg0OBa83a6gwA5lV54r~CQjUZIBPb1-PZoK4HTJlF5uo2gIFS1DpexjsC~nawjwHDM8V-ybDPDDY14Px2Rdjh72JI1CuXt~uzPH20OQacifogxJng97IXMLbxRrcbF2vdn7vf9pCkFPunH5RTC7fstELVNbz1iS1BugX1XXwL4vF6uDVP-X1vNA~ZT69xQH~qufUMg8u2nM7NFRVy~9tsILziSyhi-HLFJpNA__"
          }
        ],
        date: "Dec 2023"
      },
      {
        companyName: "Duggup",
        position: "Co-Founder and CEO",
        joiningDate: "Nov 2023",
        companyIcon: "/logoIcon.svg",
        location: "San Francisco Bay Area",
        remote: true,
        Time: "Full-time"
      },
      {
        articles:[
          {
            articleMonth: "Oct 2023",
            articleContent: "Startup Lesson I am reflecting. Don't build for the average person",
            articleImage: "https://s3-alpha-sig.figma.com/img/19af/a12d/f27e595212d7ad397a130cdeb8ac6c5e?Expires=1710720000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=Htfr2nBE~tyspuVPCUnQaeCtZxiW2uOmS5dLkY8q3JtCmWtEKmq5jFts4iKnN1~FeEqDG-2HVx1QwDPnTOWrUwsZHY64xhJ6xnLV2h9RO46NhASPNYIQxbyjqqOVPhSSDLYo2zxcrSdfNS4~Cx17EBN~LQ89EQ2AFBQa9roumb7QbAwUA8JwtnPXe73hc2XhxDwIfyoAujuQvj-AOxBvGcXiUY-IARz4DjfD5A3-2SQ2bJSntkXXrdW6486UpfOkA1IeZ08Y~5G9po2lupn5E0a2b2Kh9so~j7cKrJIMeUF~vQD0OycxC2q4CXqI8G2p-zSRj2DZwgFYTeeE7DZ66w__"
          },
          {
            articleMonth: "Oct 2023",
            articleContent: "Your biggest regrets at 80 will be acts of omission.",
            articleImage: "https://s3-alpha-sig.figma.com/img/fcaf/84e6/4461b5caa81a8f3d2afecfa15491ed1f?Expires=1710720000&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=fXQtZaSXvasp~3zTGMyiXjNZqwtA~hn-UiXIAZ~RftGmKw6ikeCBnHMQ2jnwa~-KUQpuwOTg1tn7rCX0beYea-rACbqAKvYYfg5adtbiyBs6L7DMwYcq9VwUDt60Uej~XnFgLKG2AIhlTqj76qehPJ1hyGV2UBkUr6Puu9NWXCN6ze3mxNNutcK-gsdC60w5o~jpfejvnLG3mxOvWmOLq9HYQKxUjt~9DB0u7tilC4GyfIlmbOYcRSBDLJUFJ0KrmxPT3oOAacVh6K~QH3JU9N94VQqdgysKs0g-T5IqVBYn0TAVVaE6pS4bs6zoQvNkb1KJDfQzuT2~-wOKRkiisg__"
          }
        ],
        date: "Oct 2023"
      },
      {
        companyName: "BetterUp",
        position: "VP Engineering",
        joiningDate: "Sept 2023",
        companyIcon: "/betterUpIcon.svg",
        location: "San Francisco Bay Area",
        remote: false,
        Time: "Full-time"
      }
    ]
  };

</script>

<Header userData={userData} />

<div class="xl:px-24 lg:px-16 md:px-12 sm:px-8 px-5 my-2 bg-[#FCFCFF] h-full overflow-y-auto items-center justify-center">
  <UserProfile userData={userData} />
  <div class="flex flex-col max-lg:items-center">
    {#each userData.pastExperience as object}
      {#if 'date' in object}
        <UserArticleComponent userArticles={object} />
      {:else}
        <UserExperienceComponent userExp={object} />
      {/if}
    {/each}
  </div>
  
  
</div>
