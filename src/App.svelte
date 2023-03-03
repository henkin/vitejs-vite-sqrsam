<script lang="ts">
  import 'bootswatch/dist/darkly/bootstrap.min.css';
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'
  import { Button, Container, Modal, Card, Row, Col } from 'sveltestrap';
  let isOpen = false;
  const toggle = () => (isOpen = !isOpen);
</script>

<main>
  <Container fluid>
    <Row>
      <Col>
      <Card class="col-5 ml-auto">
        <img src="https://i.ytimg.com/vi/NUJIRujygvY/hqdefault.jpg" class="card-img-top" alt="...">
        <div class="card-body">
          <h5 class="card-title">Card title</h5>
          <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">An item</li>
          <li class="list-group-item">A second item</li>
          <li class="list-group-item">A third item</li>
        </ul>
        <div class="card-body">
          <a href="#" class="card-link">Card link</a>
          <a href="#" class="card-link">Another link</a>
        </div>
          <Button color="primary" on:click={toggle}>Hello World!</Button>
          <Modal body {isOpen} {toggle} header="Hello World!">
            <p>There's a song that we're singing. Come on</p>
            <img
              src="https://i.ytimg.com/vi/NUJIRujygvY/hqdefault.jpg"
              alt="Come on Get Happy"
              class="img-fluid"
            />
          </Modal>
      </Card>      
      </Col>


    </Row>

  </Container>

</main>

<style>

</style>