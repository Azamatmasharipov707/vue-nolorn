<template>

    <section class="delivery">
        <div class="container">
            <h2 class="delivery__title title">Online Store of <span class="title-span">Production With Delivery</span></h2>

            

                <p class="delivery__text"><span class="title-span">Lorem Ipsum</span>  is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.</p>
                
                
                <p><span class="title-span">Lorem Ipsum</span>  is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.</p>
            

            <div>

                <h4>Assortment Nolorn</h4>
                
                
                <p><span class="title-span">Lorem Ipsum</span>  is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.</p>
                
                <ul class="delivery__list">
                    <li class="list__item"><a href="#!">Berries</a> </li>
                    <li class="list__item"><a href="">Dried fruits </a> </li>
                    <li class="list__item"><a href="">Spices</a> </li>
                    <li class="list__item"><a href="">Flour and cereals</a> </li>
                    <li class="list__item"><a href="">Flour and cereals</a> </li>
                    <li class="list__item"><a href="">Vegeta bles</a> </li>
                </ul>
            </div>

            

                <p class="delivery__text">Lorem Ipsum is simply <span class="title-span">dummy text</span> of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not </p>
                
                <p>Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section 1.10.32.</p>
                
            
            </div>
            
    </section>

</template>

<script setup>

</script>

<style lang="scss" scoped>

.delivery{
    .container{
        .delivery__title{
            width: 578px;
            text-align: center;
            margin: 0 auto 30px;
        }

        .delivery__text{
            font-size: 14px;
            line-height: 17px;
            font-weight: 500;
            color: var(--black);
            margin-bottom: 10px;
        }
        p{
            font-size: 14px;
            font-weight: 500;
            line-height: 17px;
            color: var(--black);
        }
        div{
            margin: 20px 0;

            h4{
                font-size: 20px;
                line-height: 23px;
                font-weight: 500;
                color: var(--title);
                margin-bottom: 20px;

            }

            p{
                font-size: 14px;
                line-height: 17px;
                font-weight: 500;
                color: var(--black);
                margin-bottom: 20px;
            }

            .delivery__list{
                margin-left: 20px;
                .list__item{
                    list-style: disc;
                    a{
                        
                        color: var(--black);
                        font-size: 14px;
                        font-weight: 500;
                        line-height: 24px;
                        &:hover{
                        color: var(--link-hover);
                    }
                        cursor: pointer;
                    } 
                }
            }
        }



    }


}

</style>