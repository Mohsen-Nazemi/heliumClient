<template>
  <Header></Header>
  <router-view></router-view>
  <Footer></Footer>
</template>


<script>
  import Header from '@/components/TheHeader'
  import Footer from '@/components/TheFooter'
  export default {
    name: 'App',
    components:{
      Header,
      Footer
    }
  }
</script>

<style>
@font-face {
    font-family: 'Bahij';
    src: url('./assets/fonts/bahij/bahij_helvetica_neue_roman_by_bahijvirtualacademy_dammd50.ttf');
    font-weight: normal;
    font-style: normal;
}

* {
    padding: 0px;
    margin: 0px;
    box-sizing: border-box;
    direction: rtl;
}

html {
    font-size: 12px
}

body {
    margin: 0px;
    font-family: Bahij;
    background-color: #fafafa;
    color: #28394f;
}

input,
textarea,
button {
    font-family: inherit
}

li {
    list-style: none;
}

a {
    text-decoration: none;
    color: inherit;
}

/* ==================================Header=============================== */
.header {
    padding: 0.75rem 1.5rem 0.6875rem 1.5rem;
    box-shadow: 0 4px 4px 0 rgba(0, 0, 0, 0.05);
}

.headerContainer {
    width: 100%;
    display: flex;
    justify-content: space-between;
    margin-bottom: 0.625rem;
    display: flex;
    align-items: center;
}

.logo__img {
    height: 2.625rem;
    width: 7.788rem;
}

.userOption {
    display: flex;
    align-items: center;
}

.userOption>*:not(:last-child):not(:first-child) {
    margin-left: 1.5625rem;
    height: 1.5rem;
    width: 1.5rem;
}

.formSearch {
    display: flex;
    align-items: center;
    height: 2.5rem;
    margin-left: 1.5625rem;
}


.searchBtn,
.goSearch {
    height: 1.5rem;
    width: 1.5rem;
    cursor: pointer;
}


.searchBox {
    display: flex;
    align-items: center;
    border: solid 1px rgba(19, 158, 202, 0.3);
    border-radius: 0.625rem;
    padding: 0.375rem 0.6875rem;
    background-color: #fff;
    margin-left: 0.9375rem;
    position: absolute;
    top: 60px;
    left: 0;

}

.formSearch {
    display: flex;
    flex-direction: row-reverse;
}

.searchCheckbox {
    display: none;
}

.searchCheckbox+.searchBox {
    display: none;
}

.searchCheckbox:checked+.searchBox {
    display: flex;
}

.formSearch input {
    height: 1.75rem;
    border: none;
    border-right: 1px solid rgba(19, 158, 202, 0.3);
    margin-right: 0.625rem;
    padding-right: 0.3125rem;
}

.formSearch input:focus {
    outline: none !important;
}

.userAvatar {
    position: relative;
    height: 2.5rem;
    width: 2.5rem;
}

.dd__user {
    padding: 1.25rem 1.875rem 1.25rem;
}

.userName {
    margin-bottom: 0.625rem;
}

.userName {
    font-size: 1rem;
}

.userId {
    font-size: 0.875rem;
}

.dd-list {
    padding-top: 1.5625rem;
    position: absolute;
    width: 15.8125rem;
    top: 100%;
    left: 0%;
    display: none;
    transition: height 0.3s ease-in-out;
    z-index: 1000;
}

.dd-list ul {
    background-color: #fff;
    position: relative;
    border-radius: 5px;
    box-shadow: 0 2px 8px 0 rgba(0, 0, 0, 0.1);
}

.dd-list ul li:not(:last-child) {
    border-bottom: 1px solid rgba(0, 0, 0, 0.15);
}

.dd-list ul li a {
    display: flex;
    padding: 0.875rem 1.875rem 0.875rem 0;
}

.dd-list ul li img {
    width: 1.5rem;
    margin-left: 1.25rem;
}

.dd-list ul li:not(:first-child):hover {
    background-color: #eef2f3;
}

.dd-list ul::before {
    position: absolute;
    left: 3%;
    top: -0.625rem;
    content: '';
    display: block;
    width: 1.25rem;
    height: 1.25rem;
    background-color: #fff;
    transform: rotate(45deg);
}

.userAvatar:hover>.dd-list {
    display: block;
}

.login__button {
    font-size: 1.125rem;
    cursor: pointer;
    color: #fff;
    width: 10.313rem;
    height: 2.5rem;
    padding: 0.25rem 2.25rem 0.375rem;
    border-radius: 10px;
    border: 1px solid #30bfb7;
    background-color: #30bfb7;
}


/* =============================Main Section=============================== */

.mainContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0 1.5rem;
}

.mainHeader {
    width: 100%;
}

.selectedTopics {
    font-size: 1.125rem;
    display: flex;
    flex-wrap: wrap;
    padding-top: 1.875rem;
}

.selectedTopics>* {
    margin: 0.625rem 1.1875rem 0.625rem 1.1875rem;
}

.selectedTopics>div:first-child {
    margin-right: 0;
}

.selectedTopics>div:not(:first-child):not(:last-child) {
    background-color: #eef2f3;
    padding: 0.25rem 0.9375rem;
    border-radius: 1.0625rem;
}

.selectedTopics__addBtn {
    width: 2rem;
    height: 2rem;
    background-color: #30bfb7;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.875rem;
    color: #fff;
    cursor: pointer;
}

.removeTopic {
    display: none;
    cursor: pointer;
}

.selectedTopics__topic:hover .removeTopic {
    display: inline;
    margin: 0.3125rem 0.3125rem 0.3125rem 0;

}

.cardsMenu {
    width: 100%;
    display: flex;
    margin-top: 1.875rem;
    border-bottom: 1px solid rgba(19, 158, 202, 0.3);
    font-size: 1.125rem;
}

.cardsMenu>* {
    margin-left: 1.1875rem;
    padding-bottom: 0.9688rem;
}



.cardsMenu__label--active {
    border-bottom: 1px solid #139eca;
    color: #139eca;
    font-weight: bold;

}




.postCard {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    align-items: center;
    padding: 1rem;
    max-width: 375px;
    margin: 2.5rem auto 0 auto;
    border-radius: 8px;
    box-shadow: 0 0 5px 1px rgba(0, 0, 0, 0.1);
}

.postHeader {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 1.8125rem;
}

.postAuthor {
    display: flex;
    align-items: center;

}

.postAuthor__avatar {
    height: 1.875rem;
    width: 1.875rem;
    margin-left: 0.9375rem;
}


.postAuthor__avatar img,
.userAvatar img {
    width: 100%;
    border-radius: 50%;
    object-fit: cover;
}

.card-user-name {
    font-size: 0.875rem;
}

.follow {
    font-size: 0.875rem;
    color: #139eca;
    border: solid 1.5px #139eca;
    border-radius: 6px;
    padding: 0 0.375rem 0.0625rem;
}

.postTitle {
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    margin-top: 1.25rem;
    font-size: 1.25rem;
    line-height: 1.5;
    overflow: hidden;
    text-overflow: ellipsis;
    text-align: right;
    font-weight: bold;
}

.postDescription {
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    height: 3rem;
    overflow: hidden;
    text-overflow: ellipsis;
    font-size: 1rem;
    line-height: 1.5;
    text-align: right;
    margin-top: 0.3125rem;
}

.postInfo {
    display: flex;
    font-size: 0.75rem;
    color: #5a5a5a;
    margin-top: 1.375rem;
    align-items: center;
}

.postDate::after,
.postTimeStudy::after {
    content: '';
    display: inline-block;
    height: 0.1875rem;
    width: 0.1875rem;
    border-radius: 50%;
    margin: 0 0.625rem;
    background-color: #707070;

}


.postCategory {
    margin-left: 0.9375rem;
    background-color: #eef2f3;
    border-radius: 17px;
    padding: 0.125rem 0.6875rem 0.1875rem 0.75rem;
}

.postBookmark,
.postLike {
    border: none;
    background-color: transparent;
}

.postBookmark img,
.postLike img {
    height: 1.5rem;
    width: 1.5rem;
    object-fit: contain;
    margin-right: 10px;
}


.postCard__cover {
    /* width: 100%; */
    order: -1;
    max-width: 100%;
    min-height: 150px;
    max-height: 303px;
    max-width: 458px;
}

.postCard__cover img {
    width: 100%;
    border-radius: 0.3125rem;
}

.postCard__img {
    position: relative;
}

.postCard:hover .postCard__img::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 98%;
    background-color: rgba(48, 191, 183, 0.9);
    opacity: 0;
    border-radius: 5px;
    transition: .5s ease;
    opacity: 0.23;
}

.postCard:hover .postTitle {
    color: #30bfb7;
}


/* ---single page--- */
.singleContainer {
    line-height: 2;
}

.singleContainer .postHeader {
    justify-content: start;
}

.singleContainer .postAuthor__name {
    margin-left: 1.5rem;
}

.postImage {
    margin: 1.25rem 0 0.625rem 0;
}

.postImage img {
    width: 100%;
    border-radius: 5px;
}

.postText {
    font-size: 1.125rem;
    margin: 1.25rem 0 0.625rem 0;
}

.authorOtherPosts .cardsMenu__label {
    border-bottom: 1px solid #139eca;
}

/* --postSuggestion */
.singleContainer .cardsMenu .cardsMenu__label {
    font-weight: bold;
    border-bottom: 1px solid #139eca;
}


.postSuggestion .postCard {
    align-items: start;
    margin-top: 1.875rem;
}

.postSuggestion .postCard .postTitle {
    margin-top: 5px;
    -webkit-line-clamp: 3;
    line-height: 2;
    height: auto;
}


/* ==========================Footer================================== */

.footer-container {
    background-color: rgb(35, 47, 61);
    background-image: url('./assets/images/Pattern.svg');
    position: relative;
    display: flex;
    justify-content: space-around;
    align-items: center;
    width: 100%;
    color: #fff;
    margin-top: 6.25rem;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    flex-wrap: wrap;
    padding-bottom: 2.44rem;

}

.footer-container::before {
    content: "";
    top: 0;
    left: 0;
    position: absolute;
    height: 100%;
    width: 100%;
    background: linear-gradient(to right, rgba(35, 47, 61, 0) 0%, rgba(35, 47, 61, .6)40%, rgba(35, 47, 61, 1) 100%);
    border-top-right-radius: 10px;

}

.footer-container div,
.footer-list {
    filter: brightness(100);
    margin: 2.5rem 2rem 0;

}

.footer-logo {
    width: 7.2875rem;
    height: 2.625rem;
}

.footer-logo img {
    width: 100%;

}

.footer-desc {
    text-align: justify;
}

.footer-list {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

.footer-list li {
    display: inline-block;
    font-size: 1.125rem;
    margin-top: 1rem;
}

.footer-list li:not(:last-child) {

    margin-left: 3.6875rem;

}

.commentItem {
    margin-top: 1.25rem;
    padding-bottom: 1.25rem;
    border-bottom: 1px solid rgba(19, 158, 202, 0.3);
}

.comment__info {
    display: flex;
    justify-content: space-between;
}

.commentItem img {
    width: 24px;
    height: 24px;
}

.comment__info__right,
.comment__info__left {
    display: flex;
}


.comment__like {
    margin-left: 1.25rem;
    display: flex;
}

.comment__info__right {
    color: #5a5a5a;
    font-size: 12px;
}

.comment__date::after {
    content: '';
    display: inline-block;
    height: 0.1875rem;
    width: 0.1875rem;
    border-radius: 50%;
    margin: 0 0.625rem;
    background-color: #707070;
}

.comment__like__count {
    color: #139eca;
    font-size: 12px;

}

.replyComment {
    margin-right: 97px;
}


.formComment .formCommentTop>* {
    display: flex;
    flex-direction: column;
    margin-bottom: 1.25rem;
}

.formComment .formCommentTop {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.formComment {
    display: flex;
    flex-direction: column;
    margin-top: 1.25rem;
}

.formComment input {
    border: solid 1px rgba(19, 158, 202, 0.3);
    border-radius: 10px;
    height: 3.125rem;
}


.formComment__name {
    width: 22%;
    min-width: 150px;
}

.formComment__family {
    width: 22%;
    min-width: 200px;
}

.formComment__email {
    width: 47%;
    min-width: 300px;
}

#txtArea {
    width: 100%;
    height: 6.25rem;
    border: solid 1px rgba(19, 158, 202, 0.3);
    border-radius: 10px;
}

.submitForm {
    width: 10.3125rem;
    background-color: #30bfb7;
    color: #fff;
    align-self: flex-end;
    margin-top: 1.25rem;
    font-size: 1.125rem;
    font-weight: bold;
}

/* =====================Media Query=================== */
/* -------Small devices (landscape phones, 576px and up) */
@media (min-width: 576px) {
    .postCard {
        flex-direction: row;
        padding: 0;
        max-width: unset;
        box-shadow: none;
    }

    .postCard__cover {
        order: 0;
        width: 40.1%;
    }

    .postCard__content {
        width: 48.6%;
    }

    .footer-desc {
        width: 38.6875rem;
        height: 3.25rem;
    }

    .footer-list li {
        margin-top: 0;
    }

    .searchBox {
        position: static;
    }

    /* --postSuggestion */

    .postSuggestion .postCard .postCard__cover {
        width: 34.9%;
    }

    .postSuggestion .postCard .postCard__content {
        width: 61%;
    }
}

/* -------Medium devices (tablets portrait, 768px and up) */
@media (min-width: 768px) {
    html {
        font-size: 14px
    }

    .secondaryAlignment {
        min-width: 750px;
        max-width: 40%;
    }

    .postCard__description {
        line-height: 2;
        height: 4rem;
    }

    .formComment .formCommentTop {
        flex-direction: row;
    }
}

/* -------(tablet landscape, 992px and up) */
@media (min-width: 992px) {
    .postTitle {
        line-height: 2;
        height: 5rem;
    }

    .postDescription {
        line-height: 2;
        height: 4rem;
    }
}

/* ------(laptop, 1200px and up) 12.5 inch and up */
@media (min-width: 1200px) {
    .primaryAlignment {
        width: 59.4%;
        min-width: 1140px;
        margin: auto;
    }

    html {
        font-size: 16px;
    }
}

/* --------- (Desktop, 1680 and up) 17.5 inch and up */
@media (min-width: 1680px) {
    .header {
        padding: 0.75rem 0;
    }

    .dd-list {
        left: -295%;

    }

    .dd-list ul::before {
        left: 50%;
    }

    .postCard {
        max-height: 303px;
    }


    .footer-desc {
        width: 38.6875rem;
        height: 3.25rem;
    }
}

/*-------- (Desktop, 1920 and up) 20 inch monitor and up*/
@media (min-width: 1920px) {}
</style>
