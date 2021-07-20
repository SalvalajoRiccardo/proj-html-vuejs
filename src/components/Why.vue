<template>
    <div>
        <h2>Why my Courses?</h2>
        <div class="why-box d-flex justify-content-center">
            <div>
                <div class="card-w">
                    <div class="img-w">
                        <i class="fas fa-briefcase"></i>
                    </div>
                    <div>
                        <h3>Entrepreneurship</h3>
                        <p>Vestibulum vitae aliquam nunc. Suspendisse mollis metus ac tellus egestas pharetra. Suspendisse at viverra purus. Pellentesque nec posuere ligula, eu congue leo. Integer vulputate tempor arcu. Vestibulum vulputate</p>
                    </div>
                </div>
                <div class="card-w">
                    <div class="img-w">
                        <i class="fas fa-thumbs-up"></i>
                    </div>
                    <div>
                        <h3>Productivity</h3>
                        <p>Vestibulum vitae aliquam nunc. Suspendisse mollis metus ac tellus egestas pharetra. Suspendisse at viverra purus. Pellentesque nec posuere ligula, eu congue leo. Integer vulputate tempor arcu. Vestibulum vulputate</p>
                    </div>
                </div>
            </div>

            <div>
                <div class="card-w">
                    <div class="img-w">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <div>
                        <h3>Accelerated learning</h3>
                        <p>Vestibulum vitae aliquam nunc. Suspendisse mollis metus ac tellus egestas pharetra. Suspendisse at viverra purus. Pellentesque nec posuere ligula, eu congue leo. Integer vulputate tempor arcu. Vestibulum vulputate</p>
                    </div>
                </div>
                <div class="card-w">
                    <div class="img-w">
                        <i class="fas fa-cog"></i>
                    </div>
                    <div>
                        <h3>Life Coaching</h3>
                        <p>Vestibulum vitae aliquam nunc. Suspendisse mollis metus ac tellus egestas pharetra. Suspendisse at viverra purus. Pellentesque nec posuere ligula, eu congue leo. Integer vulputate tempor arcu. Vestibulum vulputate</p>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name:'Why'
}
</script>

<style lang="scss" scoped>
    h2{
        margin: 100px 0;
        text-align: center;
        font-family: 'Roboto Slab', serif;
        font-size: 50px;
        font-weight: 600;
    }
    .why-box{
        
        .card-w{
            width: 500px;
            margin: 40px 20px;
            padding: 40px 20px;
            display: flex;
            border-left: 5px solid #f2b91e;
            box-shadow: 0px 2px 3px 0px #888888;
            transition: 0.5s;
            .img-w{
                margin: 0px 30px;
                i{
                    color: #f2b91e;
                    font-size: 40px;
                    transition: 0.5s;
                }
            }
            h3{
                font-family: 'Roboto Slab', serif;
                font-weight: 600;
            }
            p{
                color:grey;
                line-height: 30px;
            }
            &:hover{
                background-color: #f2b91e;
            }
            &:hover i{
                color: white;
            }
            &:hover{
                p{
                    color: black;
                }
            }
        }
    }
</style>