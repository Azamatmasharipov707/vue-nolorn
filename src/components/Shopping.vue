<template>
    <section class="shopping">
        <div class="container">
            <div class="shopping__info">
                <h2>Stay home & get your daily needs from our shop</h2>
                <p>Start You'r Daily Shopping with <span class="title-span">Nolorn</span></p>
                
                  <form action="">
                    <div class="email">
                        
                        <input type="email" placeholder="Enter your email address" required>
                    </div>
                    <div class="number">
                        
                        <input type="tel" placeholder="Enter your phone number" required>
                    </div>
                    <button>Subscribe</button>

                      
                    </form>
                    

            </div>
            <img src="../image/Shopping/kuryer.png" alt="">
        </div>
    </section>
</template>

<script setup>

</script>

<style lang="scss" scoped>

.shopping{
    margin: 80px 0;
    .container{
        display: flex;
        // align-items: center;
        justify-content: space-between;
        padding: 44px 55px;
        background: #e1f5fa;

        .shopping__info{
            h2{
                font-size: 40px;
                font-weight: 500;
                line-height: 47px;
                color: var(--black);
                font-family: var(--f_Uniform) ;
            }

            p{
                font-size: 14px;
                line-height: 17px ;
                color: var(--text);
                font-weight: 400;
                margin: 30px 0;

            }
            
            form{
                .email{
                    input{
                        max-width: 417px;
                        width: 100%;
                        padding: 10px;
                        color: var(--text);
                        border-radius: 5px;
                        background: var(--white);
                        font-family: var(--f_Uniform);

                    }
                }

                .number{
                    input{
                        max-width: 417px;
                        width: 100%;
                        padding: 10px;
                        color: var(--text);
                        border-radius: 5px;
                        background: var(--white);
                        font-family: var(--f_Uniform);
                        margin: 20px 0;

                    }


                }

                button{
                    max-width: 417px;
                    width: 100%;
                    text-align: center;
                    padding: 10px;
                    color: var(--white);
                    background: var(--link-hover);
                    border-radius: 3px;
                    transition: .5s;
                    &:hover{
                        box-shadow: 2px 4px 10px rgba(0, 0, 0, 0.274);
                    }
                }

            
                
            }


        }
    }
}
</style>