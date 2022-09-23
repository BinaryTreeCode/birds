<script>
  import { CircleBufferGeometry, MeshStandardMaterial, BoxBufferGeometry, DoubleSide } from 'three'
  import { DEG2RAD } from 'three/src/math/MathUtils'
  import {
    AmbientLight,
    Canvas,
    DirectionalLight,
    Group,
    HemisphereLight,
    Mesh,
    OrbitControls,
    PerspectiveCamera
  } from '@threlte/core'
  import { spring } from 'svelte/motion'
  import { GLTF } from '@threlte/extras'

  const scale = spring(1)
</script>

<div>
  <Canvas>
    <PerspectiveCamera position={{ x: 50, y: 1, z: 1 }} fov={26}>
      <OrbitControls
        maxPolarAngle={DEG2RAD * 80}
        autoRotate={false}
        enableZoom={false}
        target={{ y: 0.5 }}
      />
    </PerspectiveCamera>

    <DirectionalLight shadow position={{ x: 3, y: 10, z: 10 }} />
    <DirectionalLight position={{ x: -3, y: 10, z: -10 }} intensity={0.2} />
    <AmbientLight intensity={0.2} />


    <GLTF castShadow receiveShadow url={'https://raw.githubusercontent.com/BinaryTreeCode/3d/master/conejo.gltf'} position={{ y: 1 }} scale={3} />
  </Canvas>
</div>

<canvas ></canvas>

<style>
  div {
    height: 100%;
    width: 100%;
  }
</style>
