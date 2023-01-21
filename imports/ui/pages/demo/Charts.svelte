<script>
    import Top from "../../include/Top.svelte";
    import Sidebar from "../../nav/Sidebar.svelte";
    import Footer from '../../include/Footer.svelte';
    import GraphLine from "./graph-tables/GraphLine.svelte";
    import GraphBar from "./graph-tables/GraphBar.svelte";
    import GraphPie from "./graph-tables/GraphPie.svelte";
    import { onMount } from 'svelte';

    onMount(async (promise) => {
    });
</script>
<div class="sb-nav-fixed">
    <Top />
    <div id="layoutSidenav">
      <Sidebar />
      <div id="layoutSidenav_content">
          <main>
            <div class="container-fluid px-4">
                <h1 class="mt-4">Charts</h1>
                <ol class="breadcrumb mb-4">
                    <li class="breadcrumb-item"><a href="#/">Dashboard</a></li>
                    <li class="breadcrumb-item active">Charts</li>
                </ol>
                <div class="card mb-4">
                    <div class="card-body">
                        Chart.js is a third party plugin that is used to generate the charts in this template. The charts below have been customized - for further customization options, please visit the official
                        <a target="blank" href="https://www.chartjs.org/docs/latest/">Chart.js documentation</a>
                        .
                    </div>
                </div>
                <div class="card mb-4">
                    <div class="card-header">
                        <i class="fas fa-chart-area me-1"></i>
                        Area Chart Example
                    </div>
                    <div class="card-body">
                        <GraphLine width={'100%'} height={'30'} />
                    </div>
                    <div class="card-footer small text-muted">Updated yesterday at 11:59 PM</div>
                </div>
                <div class="row">
                    <div class="col-lg-6">
                        <div class="card mb-4">
                            <div class="card-header">
                                <i class="fas fa-chart-bar me-1"></i>
                                Bar Chart Example
                            </div>
                            <div class="card-body">
                                <GraphBar width={'100%'} height={'50'} />
                            </div>
                            <div class="card-footer small text-muted">Updated yesterday at 11:59 PM</div>
                        </div>
                    </div>
                    <div class="col-lg-6">
                        <div class="card mb-4">
                            <div class="card-header">
                                <i class="fas fa-chart-pie me-1"></i>
                                Pie Chart Example
                            </div>
                            <div class="card-body">
                                <GraphPie width={'100%'} height={'50'}/>
                                <!-- <canvas id="myPieChart" width="100%" height="50"></canvas> -->
                            </div>
                            <div class="card-footer small text-muted">Updated yesterday at 11:59 PM</div>
                        </div>
                    </div>
                </div>
            </div>
          </main>
          <Footer />
      </div>
    </div>
  </div>