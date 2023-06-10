<template>
    <div ref="particleWaveContainer" class="particle-wave"></div>
</template>
  
<script>
import ParticleWaveWrapper from '@/js/particle-wave-wrapper';

export default {
    name: 'ParticleWave',
    mounted() {
        this.initParticleWave();
    },
    beforeUnmount() {
        this.destroyParticleWave();
    },
    methods: {
        initParticleWave() {
            const pointSize = 3;
            const options = {
                uniforms: {
                    size: { type: 'float', value: pointSize },
                    field: { type: 'vec3', value: [0, 0, 0] },
                    speed: { type: 'float', value: 3 }
                },
                onResize(w, h, dpi) {
                    const position = []
                    const color = []
                    const width = 400 * (w / h)
                    const depth = 500
                    const height = 7
                    const distance = 9
                    for (let x = 0; x < width; x += distance) {
                        for (let z = 0; z < depth; z += distance) {
                            position.push(-width / 2 + x, -30, -depth / 2 + z)
                            color.push(0, 1 - (x / width) * 1, 0.5 + x / width * 0.5, z / depth)
                        }
                    }
                    if (this.uniforms) {
                        this.uniforms.field = [width, height, depth]
                        this.uniforms.size = (h / 400) * pointSize * dpi
                    }
                    if (this.buffers) {
                        this.buffers.position = position
                        this.buffers.color = color
                    }
                }
            };

            this.particleWave = new ParticleWaveWrapper(this.$refs.particleWaveContainer, options);
        },
        destroyParticleWave() {
            if (this.particleWave) {
                this.particleWave = null;
            }
        },
    },
};
</script>
  
<style scoped>
.particle-wave {
    width: 100%;
    height: 100%;
    bottom: 0;
    position: absolute;
    z-index: -999;
    background-color: transparent;
}
</style>
